<template>
    <div class="a">
        <h3>ToDoリスト</h3>
         <!-- タスク登録用のモーダルウィンドウが表示される -->
        <open-modal v-if="clickStateOfAddNewTask" @close-modal="closeModal">
        </open-modal>
        <button id="addTask" @click="openModal">タスクを新規追加</button>
        <display-task></display-task>
    </div>
</template>

<script>
import DisplayTask from '@/components/DisplayTask.vue'
import OpenModal from '@/components/OpenModal.vue'
export default {
    data(){
        return {
            clickStateOfAddNewTask: false
        }
    },
    components: {
        DisplayTask,
        OpenModal
    },
    methods: {
        openModal(){
            this.clickStateOfAddNewTask = true
        },
        closeModal(){
            this.clickStateOfAddNewTask = false
        }
    }
}
</script>

<style>
    #overRay {
        /* 要素を重ねた時の順番 */
        z-index: index 1;

        /* 画面全体を覆う設定 */
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background-color: rgba(0, 0, 0, 0.5); 

        /* 画面の中央に要素を表示させる設定 */
        margin: flex;
        align-items: center;
        justify-content: center;
    }

    #contents {
        z-index: 2;
        padding: 1em;
        /* display: block; */
        width: 100%;
        background: #fff;
    }

    #addTask {
        color: blue;
        color-scheme: blue;
        padding: 0 10px;
        background-color: #fff;
    }
</style>
