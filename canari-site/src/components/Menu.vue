<template>
    <!-- menu section -->
    <section class="menu-container" id="menu-section">
		<div class="menu-box">
			<div class="sauces">
				<h2 class="text-primary">NOS SAUCES (3000 CFA)</h2>
				<div class="menu-item">
					<p class="item-title">Sauce Gombo (Kopè)</p>
					<p class="text-secondary">
						Sauce gluante à base de gombo frais ou secs.
					</p>
				</div>
				<div class="menu-item">
					<p class="item-title">Sauce Arachide</p>
					<p class="text-secondary">
						Sauce onctueuse et parfumée à base de beurre d'arachide, de lait de
						coco, <br />
						de sauce hoisin et de sambal oelek.
					</p>
				</div>
				<div class="menu-item">
					<p class="item-title">Sauce Graine</p>
					<p class="text-secondary">
						Une sauce onctueuse et parfumée à base de noix de palme, <br />
						mijotée avec des morceaux de queue de bœuf, des crabes, des tripes
						et du poisson frais.
					</p>
				</div>
				<div class="menu-item">
					<p class="item-title">Sauce Feuille</p>
					<p class="text-secondary">
						A base de feuilles de manioc, gombo, patates ou épinards. <br />
						Mijotée avec de la viande ou du poisson fumé, des oignons, des
						tomates et des épices. <br />
						Idéale pour accompagner du riz ou du foutou
					</p>
				</div>
				<div class="menu-item">
					<p class="item-title">Sauce Tomate Cocktail</p>
					<p class="text-secondary">
						Une sauce crémeuse et piquante à base de mayonnaise, de sauce
						tomate, de Tabasco et de cognac.
					</p>
				</div>
				<div class="menu-item">
					<p class="item-title">Sauce Gouagouassou</p>
					<p class="text-secondary">
						Une sauce onctueuse et parfumée à base de deux sauces mélangées:
						<br />
						une sauce aux gombos et une sauce à l'aubergine..
					</p>
				</div>
			</div>
			<a class="btn btn-menu" @click="showModal" >VOIR MENU COMPLET</a>

            <modal :visible="modalVisible" @click="closeModal">
                <!-- hero -->
                   
                        <div class="modal-image">
                        <img src="../assets/thumbnail_image002.jpg" alt="Image du hero" />
                        </div>
                        <div class="hero-format">
                        <h2 class="section-sub space">VIVEZ UNE EXPÉRIENCE INOUBLIABLE</h2>
                        <p class="center-content">Cuisine Africaine</p>
                        <p class="center-content">Ouvert du Lundi au Dimanche</p>
						<p class="center-content">11h - 23h</p>
                        </div>
                    
                    <!-- Bouton de fermeture du modal -->
                    <!-- <span class="close-button" @click="closeModal">&times;</span> -->
                <!-- hero -->

            </modal>


		</div>
    </section>
    <!-- menu section -->
</template>

<script>
import Modal from './Modal.vue';


export default{
    name: 'Menu',
    components:{
        Modal,
    },
    data(){
        return{
            modalVisible: false,
        };
    },
    methods:{
        showModal(){
            this.modalVisible = true;
        },
        closeModal(){
            this.modalVisible = false;
        }
    }
    
}
</script>
<style scoped>
@import '../style.css';
</style>