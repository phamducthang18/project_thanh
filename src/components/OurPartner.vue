<template>
    <div class="footer-partners">
      <h4>Our Partners</h4>
      <Swiper
        :modules="[Autoplay]"
        :slides-per-view="'auto'"
        :space-between="20"
        :loop="true"
        :autoplay="{ delay: 3000, disableOnInteraction: false }"
        class="partner-slider"
      >
        <SwiperSlide v-for="(partner, index) in partners" :key="index">
          <a :href="partner.link" target="_blank">
            <img :src="partner.logo" :alt="partner.name" class="partner-logo" />
          </a>
        </SwiperSlide>
      </Swiper>
    </div>
  </template>
  
  <script setup>
  import { ref } from "vue";
  import { Swiper, SwiperSlide } from "swiper/vue";
  import "swiper/css";
  import "swiper/css/autoplay";
  import { Autoplay } from "swiper/modules";
  
  import partner1Logo from "@/assets/image/logo_partners/Amazon_Web_Services-Logo.png";
  import partner2Logo from "@/assets/image/logo_partners/AsusTek-black-logo.png";
  import partner3Logo from "@/assets/image/logo_partners/Axis_Communications_logo.png";
  import partner4Logo from "@/assets/image/logo_partners/Bosch-Logo.png";
  import partner5Logo from "@/assets/image/logo_partners/Cisco-logo.png";
  import partner6Logo from "@/assets/image/logo_partners/Dahua_Technology_logo.png";
  import partner7Logo from "@/assets/image/logo_partners/Dell_Technologies_logo.png";
  import partner8Logo from "@/assets/image/logo_partners/Google_Cloud_logo.png";
  import partner9Logo from "@/assets/image/logo_partners/Hewlett_Packard_Enterprise_logo.svg";
  import partner10Logo from "@/assets/image/logo_partners/Hikvision_logo.svg.png";
  import partner11Logo from "@/assets/image/logo_partners/IBM_logo.png";
  import partner12Logo from "@/assets/image/logo_partners/Lenovo_Global_Corporate_Logo.png";
  import partner13Logo from "@/assets/image/logo_partners/LG_logo.svg";
  import partner14Logo from "@/assets/image/logo_partners/Logitech_logo.png";
  import partner15Logo from "@/assets/image/logo_partners/logo_imou.png";
  import partner16Logo from "@/assets/image/logo_partners/logo_microsoft.jpg";
  import partner17Logo from "@/assets/image/logo_partners/Panasonic_logo_(Blue).svg.png";
  import partner18Logo from "@/assets/image/logo_partners/Philips_logo_new.png";
  import partner19Logo from "@/assets/image/logo_partners/redhat_logo.png";
  import partner20Logo from "@/assets/image/logo_partners/Salesforce.com_logo.png";
  import partner21Logo from "@/assets/image/logo_partners/SAP_2011_logo.png";
  import partner22Logo from "@/assets/image/logo_partners/VMware-logo.png";

  const partners = ref([
    { name: "Partner 1", link: "https://partner1.com", logo: partner1Logo },
    { name: "Partner 2", link: "https://partner1.com", logo: partner2Logo },
    { name: "Partner 3", link: "https://partner1.com", logo: partner3Logo },
    { name: "Partner 4", link: "https://partner1.com", logo: partner4Logo },
    { name: "Partner 5", link: "https://partner1.com", logo: partner5Logo },
    { name: "Partner 6", link: "https://partner1.com", logo: partner6Logo },
    { name: "Partner 7", link: "https://partner1.com", logo: partner7Logo },
    { name: "Partner 8", link: "https://partner1.com", logo: partner8Logo },
    { name: "Partner 9", link: "https://partner1.com", logo: partner9Logo },
    { name: "Partner 10", link: "https://partner1.com", logo: partner10Logo },
    { name: "Partner 11", link: "https://partner1.com", logo: partner11Logo },
    { name: "Partner 12", link: "https://partner1.com", logo: partner12Logo },
    { name: "Partner 13", link: "https://partner1.com", logo: partner13Logo },
    { name: "Partner 14", link: "https://partner1.com", logo: partner14Logo },
    { name: "Partner 15", link: "https://partner1.com", logo: partner15Logo },
    { name: "Partner 16", link: "https://partner1.com", logo: partner16Logo },
    { name: "Partner 17", link: "https://partner1.com", logo: partner17Logo },
    { name: "Partner 18", link: "https://partner1.com", logo: partner18Logo },
    { name: "Partner 19", link: "https://partner1.com", logo: partner19Logo },
    { name: "Partner 20", link: "https://partner1.com", logo: partner20Logo },
    { name: "Partner 21", link: "https://partner1.com", logo: partner21Logo },
    { name: "Partner 22", link: "https://partner1.com", logo: partner22Logo },
  ]);
  </script>
  
  <style scoped>
  .footer-partners {
    text-align: center;
    padding: 20px;
    background: #f9f9f9;
    border-radius: 10px;
  }
  
  h4 {
    margin-bottom: 15px;
    font-size: 1.5rem;
    font-weight: bold;
    color: #333;
  }
  
  .partner-slider {
    margin-top: 50px;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  
  .partner-logo {
    width: 200px;
    height: auto;
    transition: transform 0.3s ease, opacity 0.3s ease;
  }
  
  .partner-logo:hover {
    transform: scale(1.1);
    opacity: 0.8;
  }
  </style>
  