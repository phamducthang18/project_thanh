<template>
    <div class="container">
        <div class="content-header">
            <img src="../assets/image/logo.jpg" alt="" class="logo">
            <div class="menu">
                <div class="content"
                     @mouseenter="onHover(true, 'hover1')" 
                     @mouseleave="onHover(false, 'hover1')">
                    <p>Profile</p>
                    <img :src="hoverStates.hover1 ? arrowUp : arrowDown" alt="">
                    <transition name="fade-slide">
                        <div class="dropdown" v-show="hoverStates.hover1">
                            <div><a href="#">History</a></div>
                            <div><a href="#">Strategy</a></div>
                            <div><a href="#">Core Value</a></div>
                        </div>
                    </transition>
                </div>
                <div class="content"
                     @mouseenter="onHover(true, 'hover2')" 
                     @mouseleave="onHover(false, 'hover2')">
                    <p>IT Service</p>
                    <img :src="hoverStates.hover2 ? arrowUp : arrowDown" alt="">
                    <transition name="fade-slide">
                        <div class="dropdown" v-show="hoverStates.hover2">
                            <div><a href="#">Computer accessory</a></div>
                            <div><a href="#">IT infrastructure</a></div>
                            <div><a href="#">Cloud</a></div>
                            <div><a href="#">IT consulting</a></div>
                        </div>
                    </transition>
                </div>
                <div class="content"
                     @mouseenter="onHover(true, 'hover3')" 
                     @mouseleave="onHover(false, 'hover3')">
                    <p>Education Service</p>
                    <img :src="hoverStates.hover3 ? arrowUp : arrowDown" alt="">
                    <transition name="fade-slide">
                        <div class="dropdown" v-show="hoverStates.hover3">
                            <div><a href="#">Germany</a></div>
                            <div><a href="#">Canada</a></div>
                            <div><a href="#">America</a></div>
                            <div><a href="#">Australia</a></div>
                        </div>
                    </transition>
                </div>
                <div class="content"
                     @mouseenter="onHover(true, 'hover4')" 
                     @mouseleave="onHover(false, 'hover4')">
                    <p>Support</p>
                    <img :src="hoverStates.hover4 ? arrowUp : arrowDown" alt="">
                    <transition name="fade-slide">
                        <div class="dropdown" v-show="hoverStates.hover4">
                            <div><a href="#">Contact support</a></div>
                            <div><a href="#">Community</a></div>
                        </div>
                    </transition>
                </div>
                <div class="content"
                     @mouseenter="onHover(true, 'hover5')" 
                     @mouseleave="onHover(false, 'hover5')">
                    <p>E-commerce</p>
                    <img :src="hoverStates.hover5 ? arrowUp : arrowDown" alt="">
                </div>
            </div>    
            <div class="content">
                <img class="icon" src="../assets/image/headset.svg" alt="">
                <span>Contact Us</span>
            </div>
            <div class="content">
                <img class="icon" src="../assets/image/earth.svg" alt="">
                <span>VN/EN</span>
                <img :src="arrowDown" alt="">
            </div>
        </div> 
    </div>
</template>

<script setup>
import { reactive } from 'vue';
import arrowUp from '../assets/image/arrow-up.svg';
import arrowDown from '../assets/image/arrow-down.svg';

const hoverStates = reactive({ hover1: false, hover2: false, hover3: false, hover4: false, hover5: false });

const onHover = (state, key) => {
    hoverStates[key] = state;
};
</script>

<style scoped>
.icon {
    width: 20px;
}
.container {
    position: fixed;
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100%;
    top: 0;
    /* padding: 10px 35px; */
    background: white;
    /* border-bottom: 1px solid #ccc; */
    z-index: 1000;
    /* background-color: rgba(233, 69, 96, 0.8); */
}

.logo {
    width: 100px;
    margin-right: 20px;
}

.menu {
    display: flex;
    gap: 20px;
}

.content {
    position: relative;
    padding: 10px;
    cursor: pointer;
    display: flex;
    align-items: center;
    gap: 5px;
}

.content-header {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 10px;
}

.dropdown {
    position: absolute;
    top: 100%;
    left: 0;
    background: white;
    padding: 10px;
    border-radius: 8px;
    box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.2);
    min-width: 150px;
    opacity: 0;
    transform: translateY(10px);
    transition: opacity 0.3s ease, transform 0.3s ease;
    z-index: 10;
}

.content:hover {
    border-radius: 10px; 
    background-color: beige;
}

.content:hover .dropdown {
    opacity: 1;
    transform: translateY(0);
}

.dropdown div {
    padding: 8px 12px;
}

.dropdown a {
    text-decoration: none;
    color: #333;
    font-size: 14px;
    transition: color 0.3s ease;
}

.dropdown a:hover {
    color: #007bff;
}

.fade-slide-enter-active,
.fade-slide-leave-active {
    transition: opacity 0.3s ease, transform 0.3s ease;
}

.fade-slide-enter-from,
.fade-slide-leave-to {
    opacity: 0;
    transform: translateY(10px);
}

</style>
