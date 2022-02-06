<template>
    <div id="app">
        <Header/>
        <router-view />
    </div>
</template>

<script>
    import Header from "./components/Header";
    export default {
        name: 'App',
        data() {
            return{
                user:[{
                    name:"Olga"
                }],
                beer:[{
                    name:'Темное'
                }]
            }
        },
        components: {
            Header,

        }
    }

</script>
<style lang="scss">
    html, body {
        margin: 0;
        padding: 0;

        /*display: flex;*/
        /*justify-content: center;*/

    }
    h2{

    }

    #app {
        font-family:"Calibri Light", Avenir, Helvetica, Arial, sans-serif;
        max-width: 1280px;
        width: 100%;
        margin: auto;
        display: flex;
        flex-direction: column;
        align-content: center;

    }
</style>


