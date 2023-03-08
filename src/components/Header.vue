<template>
    <header>
        <h1>{{ title }}</h1>
        <p>{{ msg }}</p>    
    </header>
</template>

<script>
    export default {
        name: "Header",

        data(){
            return {
                title: "Caroline JUSTAFRE",
                msg: "Portfolio d'une développeuse WEB"
            }
        }
    }
</script>

<style scoped>
    header {
        margin: 2em auto;
    }

    h1 {
        font-weight: bold;
        padding-bottom: 0.5em;
    }

    @media screen and (max-width:425px) {
        p{
            font-size: 0.8em;
        }
    }

    @media screen and (max-width:280px) {
        h1{
            font-size: 0.8em;
        }

        p{
            font-size: 0.5em;
        }
    }
</style>