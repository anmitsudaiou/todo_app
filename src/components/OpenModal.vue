<template>
    <div id="overRay">
        <div id="contents">
            <input type="text"><br>
            <input type="date"><br>
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