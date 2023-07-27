<template>
    <section id="nav-section">
        <div class="nav-container">
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
export default{
    name: 'Navbar',
//     data: {
//     scrollPosition: null
//   },
//   methods: {
//     updateScroll() {
//       this.scrollPosition = window.scrollY
//     }
//   },
//   mounted() {
//     window.addEventListener('scroll', this.updateScroll);
//   }
}
</script>

<style scoped>
@import '../styles/navbar.css';
</style>