<template>
    <div class="item-todo">
        <p>{{ tache }}</p>
        <div v-on:click="suppression" class="btn-supr">X</div>
    </div>    
</template>

<script>
    export default {
        name: 'TodoItem',
        props: ['tache', 'suppression']
    }
</script>

<style scoped>
    .item-todo {
        display: flex;
        margin: 0 auto;
        position: relative;
        padding: 5px 60px 5px 30px;
        font-size: 20px;
        height: 60px;
        border: 0.5px solid black;
        width: 70vw;
        margin-bottom: 30px;
        border-radius: 5px;
    }
    .btn-supr {
        position: absolute;
        top: 10px;
        right: 10px;
        background-color: red;
        padding: 2px 10px;
        border-radius: 5px;
        color: whitesmoke;
        cursor: pointer
    }

    .item-todo p {
        margin-bottom: 0 !important;
    }
</style>