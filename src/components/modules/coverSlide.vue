<template>
    <swiper
        :slides-per-view="1"
        :autoplay="{
        disableOnInteraction: false,
        }"
        :modules="modules"
        class="coverSwiper"
        >
        <swiper-slide>1</swiper-slide>
        <swiper-slide>2</swiper-slide>
        <swiper-slide> 3</swiper-slide>
        <swiper-slide> 4</swiper-slide>
        <swiper-slide> 5</swiper-slide>
        <swiper-slide> 6</swiper-slide>
        <swiper-slide> 7</swiper-slide>
        <swiper-slide> 8</swiper-slide>
        <swiper-slide> 9</swiper-slide>
    </swiper>
</template>
<script>
import { Autoplay } from "swiper";
import { Swiper, SwiperSlide } from 'swiper/vue';
import "swiper/css";


export default {
    components: {
        Swiper,
        SwiperSlide,
    },
    setup() {
        return {
        modules: [Autoplay],
        };
  },
}
</script>
<style>
.coverSwiper {
    width: 100%;
    height: 100vh;
    position: absolute;
    top: 0;
    z-index: 1;
}

.swiper-slide {
    text-align: center;
    font-size: 18px;
    width: 100%;
    height: 100%;
    background: rgba(255,255,255,0.5);

    /* Center slide text vertically */
    display: -webkit-box;
    display: -ms-flexbox;
    display: -webkit-flex;
    display: flex;
    -webkit-box-pack: center;
    -ms-flex-pack: center;
    -webkit-justify-content: center;
    justify-content: center;
    -webkit-box-align: center;
    -ms-flex-align: center;
    -webkit-align-items: center;
    align-items: center;
}
.coverSwiper .swiper-slide:nth-child(1) {
    background: url('../../assets/images/creator1.png') center center no-repeat;
}

.swiper-slide img {
    display: block;
    height: 50%;
    object-fit: cover;
}
</style>
