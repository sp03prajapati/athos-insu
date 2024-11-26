<template>
<!-- Section Title -->
<div class="container section-title" data-aos="fade-up">
        <h2>Testimonials</h2>
        <p>Necessitatibus eius consequatur ex aliquid fuga eum quidem sint consectetur velit</p>
      </div><!-- End Section Title -->

    <swiper
      :slidesPerView="'auto'"
      :spaceBetween="30"
      :pagination="{
        clickable: true,
      }"
      :modules="modules"
      class="mySwiper"
    >
      <swiper-slide><img src="../assets/ImgNew/ImageSlider/man-work-working-laptop-desk.jpg" class="testimonial-img" alt=""></swiper-slide>
      <swiper-slide><img src="../assets/ImgNew/ImageSlider/medium-shot-woman-working-laptop.jpg" class="testimonial-img" alt=""></swiper-slide>
      <swiper-slide><img src="../assets/ImgNew/ImageSlider/portrait-craftsman.jpg" class="testimonial-img" alt=""></swiper-slide>
      <swiper-slide><img src="../assets/ImgNew/ImageSlider/businessman-black-suit-makes-thumbs-up.jpg" class="testimonial-img" alt=""></swiper-slide>
      <swiper-slide><img src="../assets/ImgNew/ImageSlider/business-finance-employment-female.jpg" class="testimonial-img" alt=""></swiper-slide>
    </swiper>
  </template>
  <script>
    // Import Swiper Vue.js components
    import { Swiper, SwiperSlide } from 'swiper/vue';
  
    // Import Swiper styles
    import 'swiper/css';
  
    import 'swiper/css/pagination';
  

  
    // import required modules
    import { Pagination } from 'swiper/modules';
  
    export default {
      name: 'ImageSlider',
      components: {
        Swiper,
        SwiperSlide,
      },
      setup() {
        return {
          modules: [Pagination],
        };
      },
    };
  </script>
  <style>
#app {
  height: 100%;
}
html,
body {
  position: relative;
  height: 100%;
}

body {
  background: #eee;
  font-family: Helvetica Neue, Helvetica, Arial, sans-serif;
  font-size: 14px;
  color: #000;
  margin: 0;
  padding: 0;
}

.swiper {
  width: 100%;
  height: 100%;
}

.swiper-slide {
  text-align: center;
  font-size: 18px;
  background: #fff;

  /* Center slide text vertically */
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 10px;
}

.swiper-slide img {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: cover;
  border-radius: 10px;
}

.swiper-slide {
  width: 20%;
}

/* .swiper-slide:nth-child(2n) {
  width: 60%;
}

.swiper-slide:nth-child(3n) {
  width: 40%;
} */

</style>