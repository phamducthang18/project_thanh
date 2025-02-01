<template>
    <Swiper :modules="[Navigation, Pagination]" navigation pagination>
      <SwiperSlide v-for="(img, index) in images" :key="index">
        <img :src="img" class="slide" />
      </SwiperSlide>
    </Swiper>
</template>
<script setup>
  import { Swiper, SwiperSlide } from "swiper/vue";
  import "swiper/css";
  import "swiper/css/navigation";
  import "swiper/css/pagination";
  import { Navigation, Pagination } from "swiper/modules";
  import slide1 from "@/assets/image/";
  import slide2 from "@/assets/images/slide2.jpg";
  import slide3 from "@/assets/images/slide3.jpg";

const images = [slide1, slide2, slide3];
</script>
  
<style scoped>
.slide {
width: 100%;
border-radius: 10px;
}
</style>
  