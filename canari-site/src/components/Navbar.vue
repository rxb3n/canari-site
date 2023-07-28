<template>
    <section id="nav-section">
        <div class="nav-container" :class="{ 'scrolled': isScrolled }">
            <div class="nav-logo">
                <a href="/"><h2 class="nav logo">CANARI</h2></a>
            </div>
            <div class="nav-elements">
                <a href="#hero-section"><p class="nav">Accueil</p></a>
               <a href="#about-section"><p class="nav">A propos</p></a>

            <div class="menu-dropdown">
               <a href="#menu-section"><p class="dropbtn">Menu</p></a> 
                <div class="dropdown-content">
                    <a @click="showModal" href="#menu-section">MENU COMPLET</a>
                </div>
            </div>

                <a href="#cta-section"><p class="nav">Contact</p></a>

            </div>
            <button class="hamburger-menu" id="toggle-menu"><img src="../assets/menu-icon.png" width="40" height="40"></button>
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
@import '../style.css';
</style>