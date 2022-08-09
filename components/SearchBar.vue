
<template>
<div>
  <div class="header" id="myHeader">
  <h2 id="header-title">Booking Cambodia</h2>

  <div class="all-service">
        <swiper class="swiper" :options="swiperOption">
            <swiper-slide v-for="item in items" :key="item.id"  :src="item.img">
            <div class="header-picture">
            <img @click="goTo(item.url)" :src="item.img" />
            </div>
              <h3>{{item.title}}</h3>
            </swiper-slide>
        </swiper>
  </div>
  <div class="footer-title">
    <h1>Find your next stay </h1>
    <p>Search low prices on hotels, home and much more...</p>
  </div>
</div>
</div>
</template>

<script>
  import { Swiper, SwiperSlide } from 'vue-awesome-swiper'
  import 'swiper/css/swiper.css'

  export default {
    name: 'swiper-example-responsive-breakpoints',
    title: 'Responsive breakpoints',
    components: {
      Swiper,
      SwiperSlide
    },
    data() {
      return {
         items:[
                    { 
                        img :'/images/stay.png', 
                        title:'Stay',
                        url: '/'
                    },

                    { 
                        img :'/images/dinner.png',
                        title:'Food',
                        url: 'foodbooking'
                    },
                    { 
                        img :'/images/plan.png',
                        title:'Fly',
                        url: 'flybooking'
                    },
                    { 
                        img :'/images/car.png',
                        title:'Car',
                        url: 'carbooking'
                    
                    },
                    { 
                        img :'/images/tickets.png',
                        title:'Service',
                        url: 'servicebooking'
                    
                    },
                ],
        swiperOption: {
          slidesPerView: 5,
          spaceBetween: 10,
          pagination: {
            el: '.swiper-pagination',
            clickable: true
          },
          breakpoints: {
            1024: {
              slidesPerView: 10,
              spaceBetween: 0
            },
            768: {
              slidesPerView: 3,
              spaceBetween: 20
            },
            640: {
              slidesPerView: 5,
              spaceBetween: 0
            },
            320: {
              slidesPerView: 1,
              spaceBetween: 0
            }
          }
        }
      }
    },

    methods: {
            goTo(url) {
              console.log(url);
                this.$router.push(url);
            },
    },


  }
</script>
<style scoped>
/* .wrapper {
    width: 100%;
    height: 40vh;
    background-color: #183873;
} */
h3{
  color: #fff;
  margin:0px 0px 0px 25px;
}
.search-bar {
    padding: 25px;
    margin-left:5%;
    margin-right: 5%;
}
#search {
    width: 100%;
    padding: 10px;
}
.all-service {
  margin-top: -30px;
    padding: 25px;
    margin-left:5.5%;
    margin-right: 5%;
}
.header-picture {
  width: 90px;
  height: 60px;
  padding: 15px 0px 0px 20px;
  border-radius: 30px;
  background-color: rgb(182, 171, 171);
}
.footer-title {
  margin-left: 7%;
  font-weight: bold;
}

img {
    width: 50px;
}
p{
    color: #fff;
}
.top-container {
  background-color: #f1f1f1;
  padding: 30px;
  text-align: center;
}

.header {
  padding: 10px 16px;
  background: #183873;
  color: #f1f1f1;
  position: fixed;
  top: 0;
  width: 100%;
  z-index: 900;
}
#header-title {
  margin-left: 7%;
  font-weight: bold;
}

.content {
  padding: 16px;
}

</style>