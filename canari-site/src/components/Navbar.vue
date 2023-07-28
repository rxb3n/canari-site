<template>
    <section id="nav-section">
        <div class="nav-container" :class="{ 'scrolled': isScrolled }">
            <div class="nav-logo">
                <h2 class="nav logo">CANARI</h2>
            </div>
            <div class="nav-elements">
                <a href="/"><p class="nav">Accueil</p></a>
               <a href="/"><p class="nav">A propos</p></a>

            <div class="menu-dropdown">
               <a href="/"><p class="dropbtn">Menu</p></a> 
                <div class="dropdown-content">
                    <a href="#">MENU COMPLET</a>
                </div>
            </div>

                <a href="/"><p class="nav">Contact</p></a>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Navbar',
  data() {
    return {
      isScrolled: false
    }
  },
  created() {
    window.addEventListener('scroll', this.onScroll);
  },
  destroyed() {
    window.removeEventListener('scroll', this.onScroll);
  },
  methods: {
    onScroll(event) {
      this.isScrolled = window.scrollY > 0;
    }
  }
}
</script>

<style scoped>
@import '../styles/navbar.css';
</style>