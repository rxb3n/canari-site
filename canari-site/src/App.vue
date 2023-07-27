<template>
    <Navbar></Navbar>
    <Hero></Hero>
    <About></About>
    <Menu></Menu>
    <Contact></Contact>
    <Footer></Footer>
</template>

<script>
import About from './components/About.vue';
import Navbar from './components/Navbar.vue';
import Hero from './components/Hero.vue';
import Contact from './components/Contact.vue';
import Footer from './components/Footer.vue';
import Menu from './components/Menu.vue';


export default{
    name: 'App',
    components:{
        About,
        Navbar,
        Hero,
        Menu,
        Contact,
        Footer
    }
}
</script>

<style scoped>
@import './style.css';
</style>
