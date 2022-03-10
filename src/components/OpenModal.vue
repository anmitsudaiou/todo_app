<template>
    <div id="overRay">
        <div id="contents">
            <input placeholder="追加したいタスクを入力してください" id="taskContents" type="text"><br><br>
            <input type="date"><br><br>
            <!-- <datepicker :language="ja"></datepicker> -->
            <button @click="register">追加</button>
            <button @click="back">戻る</button>
        </div>
    </div>
</template>

<script>
export default {
    methods: {
        back(event){
            this.$emit('close-modal', event)
        }
    }
}
</script>

<style scoped>
</style>