<template>
  <Swiper
    :modules="[Navigation, Pagination, Autoplay]"
    navigation
    pagination
    :autoplay="{ delay: 3000, disableOnInteraction: false }"
  >
    <SwiperSlide v-for="(img, index) in images" :key="index" class="content-slide">
      <img :src="img.src" class="slide" />
      <div class="caption">{{ img.text }}</div>
    </SwiperSlide>
  </Swiper>
  
  <div class="inner">
    <div class="content-main">
      <img src="@/assets/image/laptop.svg" alt="" class="icon">
      <span>Human Resource</span>
    </div>
    <div class="content-main">
      <img src="@/assets/image/computer.svg" alt="" class="icon">
      <span>Education Services</span>
    </div>
    <div class="content-main">
      <img src="@/assets/image/laptop.svg" alt="" class="icon">
      <span>Human Resource</span>
    </div>
  </div>
  <div class="main-content">
    <div class="main-title">
      <h2>Vision Statement for Long Walll</h2>
    </div>
    <div class="main-inner">
    <h4 class="title-main-content">At Long Wall, we are committed to delivering cutting-edge technology solutions that empower businesses and individuals to optimize operations, enhance experiences, and drive sustainable growth across multiple industries.</h4>
    <ul>
        <li><strong>IT Services:</strong>
            <ul>
                <li>Computer Accessories – High-quality products to enhance IT performance.</li>
                <li>IT Infrastructure – Reliable and scalable systems for businesses.</li>
                <li>Cloud Solutions – Secure and efficient cloud computing services.</li>
                <li>IT Consulting – Expert guidance to streamline digital transformation.</li>
            </ul>
        </li>
        
        <li><strong>Education Services:</strong>
            <ul>
                <li>Supporting global education opportunities in:</li>
                <li>🇩🇪 Germany</li>
                <li>🇨🇦 Canada</li>
                <li>🇺🇸 United States</li>
                <li>🇦🇺 Australia</li>
            </ul>
        </li>

        <li><strong>E-commerce:</strong> 
            <ul>
                <li>Developing smart online shopping platforms that connect customers with the best products and services.</li>
            </ul>
        </li>
    </ul>
    <p><strong class="title-main-content">💡 With innovation at our core, we strive to be a trusted technology partner, helping businesses and individuals succeed in the digital era.</strong></p>
  </div>

  </div>
  <div class="inner-2">
    <a href="link1.html" class="inner-item">
      <img src="@/assets/image/it_service_panel1.png" alt="" class="img_inner">
      <span>Human Source Services</span>
      <!-- <a href="link1.html">Learn more</a> -->
    </a>
    
    <a href="link2.html" class="inner-item">
      <img src="@/assets/image/commercial_panel1.jpg" alt="" class="img_inner">
      <span>Commercial Services</span>
      <!-- <a href="link2.html">Learn more</a> -->
    </a>
    
    <a href="link3.html" class="inner-item">
      <img src="@/assets/image/education_panel1.jpg" alt="" class="img_inner">
      <span>Education Services</span>
      <!-- <a href="link3.html">Learn more</a> -->
    </a>
    
    <a href="link4.html" class="inner-item">
      <img src="@/assets/image/hr_panel1.png" alt="" class="img_inner">
      <span>HR Solutions</span>
      <!-- <a href="link4.html">Learn more</a> -->
    </a>
  </div>
  <MessageCEO/>
  <OurPartner/>
</template>

<script setup>
import MessageCEO from "@/components/MessageCEO.vue";
import OurPartner from "@/components/OurPartner.vue";
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";
import "swiper/css/navigation";
import "swiper/css/pagination";
import "swiper/css/autoplay";
import { Navigation, Pagination, Autoplay } from "swiper/modules";

import slide1 from "@/assets/image/hr_panel2.jpg";
import slide2 from "@/assets/image/education_panel2.jpg";
import slide3 from "@/assets/image/ban_xe_panel2.png";
import slide4 from "@/assets/image/it_service_panel2.jpg";

const images = [
  { src: slide1, text: "You Demand Quality, We Supply Growth" },
  { src: slide2, text: "Education is the foundation for career opportunities We offer study-abroad opportunities" },
  { src: slide3, text: "Motorbike and Car Commercial bring the most convenient for customers" },
  { src: slide4, text: "Providing infrastructure vs server, cloud services provided by enterprises" }
];
</script>

<style scoped>

.slide {
  width: 1000px;
  border-radius: 10px;
  object-fit: cover;
}

.content-slide {
  margin-top: 235px;
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  max-height: 350px;
}

.caption {
  position: absolute;
  bottom: 20px;
  left: 50%;
  transform: translateX(-50%);
  width: fit-content;
  max-width: 90%;
  background: rgba(0, 0, 0, 0.6);
  color: #fff;
  font-size: 18px;
  font-weight: bold;
  text-align: center;
  padding: 10px 20px;
  border-radius: 10px;
  white-space: nowrap;
}
.inner {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 20px;
  margin-top: 30px;
}

.content-main {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 15px;
  width: 150px;
  height: 150px;
  background: white;
  border-radius: 15px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
}

.content-main:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 15px rgba(0, 0, 0, 0.2);
}

.icon {
  width: 50px;
  height: 50px;
  margin-bottom: 10px;
}

span {
  font-size: 16px;
  font-weight: bold;
  color: #333;
}
.inner-2 {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); /* Cột co giãn linh hoạt */
  gap: 20px;
  padding: 20px;
}

.inner-item {
  display: flex;
  flex-direction: column; 
  align-items: center;
  justify-content: space-between; 
  padding: 15px;
  background: white;
  border-radius: 15px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
  overflow: hidden;
  cursor: pointer; /* Cho thấy nó có thể click */
  text-align: center;
}

.inner-item:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 15px rgba(0, 0, 0, 0.2);
}
.title-main-content {
  max-width: 930px; 
  text-align: left;
  
  margin: 30px auto !important;
  line-height: 1.5; 
}

.img_inner {
  width: 100%;
  height: 200px; 
  object-fit: cover; 
  border-radius: 10px;
}

span {
  margin-top: 10px;
  font-size: 16px;
  font-weight: bold;
  color: #333;
}

a {
  text-decoration: none;
  color: blue;
  font-size: 14px;
  margin-top: 5px;
}
.main-contnet{
  /* display: flex; */
}
.main-title{
  display: flex;
  justify-content: center;
  align-items: center;
}
.main-title h2{
  display: inline-block;
  position: relative;
  padding-bottom: 10px; 
}
.main-title h2::after {
  content: "";
  display: block;
  width: 100%;
  height: 3px;
  background-color: #E94560;
  position: absolute;
  bottom: 0;
  left: 0;
}
.main-inner{
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  /* min-height: 100vh; */
  padding: 20px; 
}
.main-inner h4{
  margin: 30px;
}
.main-inner div{
  margin: 30px 100px;
}
.main-inner ul {
    list-style: none; 
    padding: 0;
}

.main-inner ul li {
    margin-bottom: 10px; 
    font-size: 16px;
}

.main-inner ul li strong {
    color: #E94560; /* Màu nổi bật cho tiêu đề từng danh mục */
    font-size: 18px;
}

.main-inner ul li ul {
    margin-left: 20px; /* Dịch vào để tạo cấp bậc */
}

.main-inner ul li ul li::before {
    content: "✔"; /* Biểu tượng checkmark */
    color: #E94560;
    font-weight: bold;
    margin-right: 8px;
}
</style>