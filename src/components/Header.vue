<template>
    <div class="header">
        <h1>Пьяный солод</h1>
    </div>
</template>

<script>
    export default {
        name: "Header"
    }
</script>

<style scoped>
    .header {
        /*max-width: 1280px;*/
        width: 100%;
        display:flex;
        flex-direction: row;
        justify-content: center;
        background-color: rgba(210, 210, 202, 0.4);
        border-bottom: 1px #323232 solid;


    }
    h1 {
        /*border-bottom: 1px solid red;*/
        margin: 20px 0 20px 0;
        padding: 0;
    }

    @media screen and (max-width: 320px) {
        h1 {
            margin: 10px 0 10px 0;
            padding: 0;
            font-size: 20px;
        }
    }
</style>
