<template>
    <section id="gallery-section">
        <swiper
        :modules="modules"
        :slides-per-view="3"
        :space-between="50"
        navigation
        :pagination="{ clickable: true }"
        :scrollbar="{ draggable: true }"
        @swiper="onSwiper"
        @slideChange="onSlideChange"
        >
        <div class="gallery">

            <div class="gallery-img">
                <swiper-slide>Slide 1</swiper-slide>
            </div>

            <div class="gallery-img">
                <swiper-slide>Slide 2</swiper-slide>
            </div>

            <div class="gallery-img">
                <swiper-slide>Slide 3</swiper-slide>
            </div>

        </div>

        </swiper>
    </section>


  </template>



  <script>
    // import Swiper core and required modules
    import { Navigation, Pagination, Scrollbar, A11y } from 'swiper/modules';
  
    // Import Swiper Vue.js components
    import { Swiper, SwiperSlide } from 'swiper/vue';
  
    // Import Swiper styles
    import 'swiper/css';
    import 'swiper/css/navigation';
    import 'swiper/css/pagination';
    import 'swiper/css/scrollbar';
  
    // Import Swiper styles
    export default {
    name: 'Gallery',
      components: {
        Swiper,
        SwiperSlide,
      },
      setup() {
        const onSwiper = (swiper) => {
          console.log(swiper);
        };
        const onSlideChange = () => {
          console.log('slide change');
        };
        return {
          onSwiper,
          onSlideChange,
          modules: [Navigation, Pagination, Scrollbar, A11y],
        };
      },
    };
  </script>


<style scoped>
    @import '../style.css';
</style>