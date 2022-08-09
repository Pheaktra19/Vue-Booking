
<template>
<div class="wrapper">
    <div class="title">
        <h1>Most Popular</h1>
        <h3>See all</h3>
    </div>
    <div class="sub-wrapper">
      <swiper class="swiper" :options="swiperOption">
        <swiper-slide class="image" v-for="item in items" :key="item.id">
          <img :src="item.img"/>
          <h2>{{item.title}}</h2>
          <p>{{item.price}}</p>
          <div class="popular-footer">
            <div class="bed">
                <p>1 Bed</p>
                <img src="/images/iconbed.png">
            </div>
            <div class="wifi">
                <p>Wifi</p>
                <img src="/images/wifi.png">
            </div>
          </div>

          <div class="book-now">
            <center>
                <h1 @click="goTo('/payment')">Book Now</h1>
            </center>
          </div>    
        </swiper-slide>
        <!-- <div class="swiper-pagination" slot="pagination"></div> -->
      </swiper>
    </div>
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
    methods: {
      goTo(url) {
        console.log(url)
        this.$router.push(url)
        
      }
    },
    data() {
      return {
        items:[
            {
                img:'/images/bedroom.jpg',
                title:'Retro Kampot Guesthouse',
                price:'115$/night',
                

            },
            {
                img:'/images/room.jpg',
                title:'Siem Reap',
                price:'20$/night'
            },
            {
                img:'/images/roundbed.jfif',
                title:'Kam Pot',
                price:'50$/night'
            },
            {
                img:'/images/Twin-Room.webp',
                title:'Kam Pot',
                price:'79$/night'
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
    }
  }
</script>
<style scoped>
.wrapper {
  margin: 0% 5% 0% 6%;
  
}

.image {
  border: 1px solid gray;
  /* background-color: aqua; */
}
.title {
    display: flex;
    justify-content:space-between;
}
h1{
  color: blue;
}
h2{
    color: blue;
}
img {
    width: 100%;
    height: 40vh;
}
.bed{
    display: flex;
    /* justify-content: space-between; */
    width: 90px;
    height: 35px;
    background-color: gray;
    border-radius: 15px;
    padding: 5px 2px 5px 5px;
    
}
.wifi{
    display: flex;
    /* justify-content: space-between; */
    width: 90px;
    height: 35px;
    background-color: gray;
    border-radius: 15px;
    padding: 5px 2px 5px 5px;
    margin-left:15px ;
    
}

.bed img {
    margin: 2px 5px ;
    width: 30px;
    height: 30px;
}
.wifi img {
    margin: 2px 5px ;
    width: 30px;
    height: 30px;
}

.popular-footer{

    display: flex;
    flex-wrap: wrap;
    margin-left:50px ;
}
.book-now {
    width: 100%;
    height: 30px;
    background-color: red;
    padding: 0px 0px 10px 0px;
}
</style>