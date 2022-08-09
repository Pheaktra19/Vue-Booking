
<template>
<div class="wrapper">
    <h1>Explore Cambodia</h1>
    <swiper class="swiper" :options="swiperOption">
      <swiper-slide v-for="item in items" :key="item.id">
        <img @click="goTo(item.url)" :src="item.img"/>
        <center>
            <h2>{{item.title}}</h2>
        </center>
      </swiper-slide>
      <!-- <div class="swiper-pagination" slot="pagination"></div> -->
    </swiper>
  </div>
</template>

<script>
  import { Swiper, SwiperSlide } from 'vue-awesome-swiper'
  import 'swiper/css/swiper.css'

  export default {
    name: 'swiper-example-free-mode',
    title: 'Free mode / No fixed positions',
    components: {
      Swiper,
      SwiperSlide
    },
    data() {
      return {

        items:[
            {
                img:'/images/pp.png',
                title:'Phnom Penh',
                url:'/provinces/phnompenh' 
            },
            {
                img:'/images/sr.jpg',
                title:'Siem Reap',
                url: '/provinces/seimreap'
            },
            {
                img:'/images/Ratanakiri.jpg',
                title:'Ratanakiri',
                url:'/provinces/ratanakiri'
            },
            {
                img:'/images/kompot.jpg',
                title:'Kam Pot',
                url:'/provinces/kampot'
            },
            {
                img:'/images/kohkong.jpg',
                title:'Koh Kong',
                url:'/provinces/kohkong'
            },
            {
                img:'/images/preahvihea.jfif',
                title:'Preah Vihea',
                url:'/provinces/preahvihea'
            },
        ],
       
        swiperOption: {
          slidesPerView: 3,
          spaceBetween: 30,
          freeMode: true,
          pagination: {
            el: '.swiper-pagination',
            clickable: true
          },
            breakpoints: {
            1024: {
              slidesPerView: 4,
              spaceBetween: 40
            },
            768: {
              slidesPerView: 3,
              spaceBetween: 30
            },
            640: {
              slidesPerView: 2,
              spaceBetween: 20
            },
            320: {
              slidesPerView: 1,
              spaceBetween: 10
            }
          }
        }
      }
    },

     methods: {
          goTo(url) {
            console.log(url);
                this.$router.push(url);

            
          }
        },
  }
</script>
<style scoped>
.wrapper {
  margin: 5% 5% 0% 6%;
  
}
h1{
  color: blue;
}
h2{
    color: gray;
}
img {
    width: 100%;
    height: 40vh;
}
</style>