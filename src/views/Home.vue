<template>
    <section class="container">
        <Header/>
        <main class="portfolio">
            <Portfolio/>    
        </main>
    </section>
    <Footer/>
</template>

<script>
    import Header from '@/components/Header.vue'
    import Portfolio from '@/components/Portfolio.vue'
    import Footer from '@/components/Footer.vue'

    export default {
        name: 'Home',
        components: {
            Header,
            Portfolio,
            Footer
        }
    }
</script>

<style>
    .container {
        display: flex;
        flex-direction: column;
        min-height: 90vh ;
    }
    
    .portfolio {
        flex-grow: 2;
    }
</style>