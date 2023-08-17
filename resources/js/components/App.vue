<template>
    <Menu />
    <About />
    <HairCut />
    <Footer />
</template>
<script>
    import Menu from './Menu.vue';
    import About from './About.vue';
    import HairCut from './HairCut.vue';
    import Footer from './Footer.vue';

    export default{
        components:{
            Menu,
            About,
            HairCut,
            Footer
        }
    }
</script>
