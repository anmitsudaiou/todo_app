<template>
    <div id="overRay">
        <div id="contents">
            <input placeholder="タスクを入力してください" id="taskContents" type="text"><br><br>
            <input type="date" id="dateContents"><br><br>
            <!-- <datepicker :language="ja"></datepicker> -->
            <div class="button-space">
                <button id="register" @click="register">追加</button>
                <button id="back" @click="back">戻る</button>
            </div>
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
#taskContents {
    font-size: 15px;
    width: 90%;
}

#dateContents {
    width: 90%;
    text-align: center;
    font-size: 15px;
}

.button-space {
    display: flex;
    justify-content: space-around;
}

#register {
    width: 50%;
    margin-left: 4;
}

#back {
    width: 40%;
}
</style>