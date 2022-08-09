<template>
<div class="banner-wrapper">
    <h1>Special Offer</h1>
  <swiper class="swiper" :options="swiperOption">
    <swiper-slide v-for="item in items" :key="item.id">
        <img :src="item.img"/>
    </swiper-slide>
  </swiper>
  </div>
</template>

<script>
  import { Swiper, SwiperSlide } from 'vue-awesome-swiper'
  import 'swiper/css/swiper.css'

  export default {
    name: 'swiper-example-autoplay',
    title: 'Autoplay',
    components: {
      Swiper,
      SwiperSlide
    },
    data() {
      return {
        items:[
            {
                img: '/images/angkor.JPG'
            },
            {
               
               img: '/images/bg.JPG' 
            },
            {
               img: '/images/a.JPG' 
            },
            {
               img: '/images/c.JPG' 
            },
            {
               img: '/images/banner.JPG' 
            },
        ],
        swiperOption: {
          spaceBetween: 30,
          centeredSlides: true,
          autoplay: {
            delay: 2000,
            disableOnInteraction: false
          },
          pagination: {
            el: '.swiper-pagination',
            clickable: true
          },
          navigation: {
            nextEl: '.swiper-button-next',
            prevEl: '.swiper-button-prev'
          }
        }
      }
    }
  }
</script>
<style scoped>
.banner-wrapper {
    /* margin-top: -20px; */
    margin: 22% 5% 0% 6%;
    width: 90%;
    height: 50vh;
    /* background-color: green; */
    /* border: 1px solid black; */
    
}
img {
    width: 100%;
    height: 50vh;
}
h1 {
    color: blue;
}
</style>
