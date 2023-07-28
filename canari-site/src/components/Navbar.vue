<template>
    <section id="nav-section">
        <div class="nav-container" :class="{ 'scrolled': isScrolled }">
            <div class="nav-logo">
                <a href="/"><h2 class="nav logo">CANARI</h2></a>
            </div>
            <div class="nav-elements" id="nav-links">
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
            <button @click =openMenu class="hamburger-menu" id="toggle-menu"><img src="../assets/menu-icon.png" width="40" height="40"></button>
        </div>

        <div class="nav-mobile">
          <p class="mobile-element">Accueil</p>
          <p class="mobile-element">A propos</p>
          <p class="mobile-element">Menu</p>
          <p class="mobile-element">Contact</p>
        </div>

    </section>
</template>

<script>
export default {
    name: 'Navbar',
  data() {
    return {
      isScrolled: false,
      isActive: false
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
    },

    openMenu(event) {
      const toggleButton = document.getElementsByClassName('hamburger-menu')[0];
      const navLinks = document.getElementsByClassName('nav-mobile')[0];

        if (this.isActive == false) {
          navLinks.style.transform = 'translate(-100%, 0)';
          this.isActive = true;
          console.log(this.isActive)
        } else if (this.isActive == true) {
          navLinks.style.transform = 'translate(100%, 0)';
          this.isActive = false;
          console.log(this.isActive)
        }
    }
  }
}
</script>

<style scoped>
@import '../style.css';
</style>