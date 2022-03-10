<template>
    <div>
        /* v-ifとDynamo使ってDataをとってくる*/
        <h1>ここにタスクを表示</h1>
        <button @click="editTask" id="edit">編集</button>
        <button @click="deleteTask" id="delete">削除</button>
    </div>
</template>

<script>
export default {
    methods: {
        editTask(){
            //編集用コンポーネント利用
        },
        deleteTask(){
            //JSのPrompt利用
            alert('このタスクを削除してよろしいですか？')
        }
    }
}
</script>

<style scoped>
    #edit {
        color: aqua;
        background-color: white;
    }
    #delete {
        color: red
    }
</style>

