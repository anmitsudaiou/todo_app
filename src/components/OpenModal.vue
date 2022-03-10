<template>
    <div id="overRay">
        <div id="contents">
            <input placeholder="追加したいタスクを入力してください" id="taskContents" type="text"><br><br>
            <input type="date"><br><br>
            <button @click="register">追加</button>
            <button @click="clickEvent">戻る</button>
        </div>
    </div>
</template>

<script>
export default {
    methods: {
        clickEvent(event){
            this.$emit('close-modal', event)
        }
    }
}
</script>

<style scoped>
</style>