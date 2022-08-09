<template>
    <div class="wrapper">
        <div class="wrapper-above">
            <div class="left-counter">
            <div class="sub-counter">
                <div class="wrap-leftcounter">
                <h2>Search</h2>
                <p>Destination/property name:</p>
                <div class="location">
                    <select  name="cars" id="select">
                        <option value="Phnom Penh">Phnom Penh</option>
                        <option value="Takoe">Takeo</option>
                        <option value="Kampot">Kam Pot</option>
                        <option value="Kompong Chang">Kompong Chang</option>
                        <option value="Kompong Thom">Kompong Thom</option>
                        <option value="Kompong Speu">Kompong Speu</option>
                        <option value="Kror Jes">Kror Jes</option>
                        <option value="Kompong Chnang">Kompong Chnang</option>
                        <option value="Preah Vihea">Preah Vihea</option>
                        <option value="Mondol Kiri">Mondol Kiri</option>
                        <option value="Rothanak Kiiri">Rothanak Kiiri</option>
                        <option value="Pai Len">Pai Len</option>
                        <option value="Poi Pet">Poi Pet</option>
                        <option value="Prey Veng">Prey Veng</option>
                        <option value="Svay Reang">Svay Reang</option>
                        <option value="Batom Bong">Batom Bong</option>
                        <option value="Bonteay Meanchey">Bonteay Meanchey</option>
                        <option value="Odor Meanchey">Odor Meanchey</option>
                    </select>
                </div>
                <p>Check-in date</p>
                <div class="checkin-date">
                    <input id="input" type="date" placeholder="Check-In" name="usrnm"/>
                </div>
                <p>Check-out date</p>
                <div class="checkout-date">
                    <input id="input" type="date" placeholder="Check-Out" name="usrnm"/>
                </div>
                <p>Night Stay</p>
                <div class="night-stay">
                    <input id="input" type="date" placeholder="Check-Out" name="usrnm"/>
                </div>
                <div class="search">
                <form id="search-form" name="search" action="/products" method="get">
                    <input id="search" src="path/to/image" name="search" type="text" value="Search">
                </form>
                </div>
                </div>
            </div>
            </div>

            <div class="right-counter">
           <div class="picture">
                 <div class="grid-container">
                    <div class="grid-item item1">
                        <img src="/phnompenh/Delux.jfif">
                    </div>
                    <div class="grid-item item2">
                        <img src="/phnompenh/citycenter.jfif">
                    </div>
                    <div class="grid-item item3">
                        <img src="/phnompenh/naki.jfif"/>
                    </div>   
                    <div class="grid-item item5">
                        <img src="/phnompenh/d1.jpg"/>
                        <img src="/phnompenh/d2.jpg"/>
                        <img src="/phnompenh/d3.jpg"/>
                    </div>
                </div>
           </div>
            </div>
        </div>
        <div class="wrapper-below">
            <div class="description">
                <span>
                    Grand Elevation Hotel is located in Phnom Penh and features a shared lounge. 
                    Popular points of interest nearby include Eon Mall and Diamond Island Convention and Exhibition Center. 
                    The accommodations features a 24-hour front desk, airport transfers, a business center and free WiFi.
                    The rooms in the hotel are fitted with a flat-screen TV with cable channels.
                    All rooms at Grand Elevation Hotel have air-conditioning.
                    All rooms at Grand Elevation Hotel have air-conditioning.
                    All rooms at Grand Elevation Hotel have air-conditioning.
                    All rooms at Grand Elevation Hotel have air-conditioning.
                </span>
            </div>
            <div class="booking">
                <h2>Property Highlights</h2>
                <h2 id="room">Delux Hotel</h2>
                <div class="title-wrapper">
                    <div class="room">
                        <p>Room</p>
                        <h3 id="room">5 left</h3>
                        <div class="bed">
                            <p><img src="/images/bed.webp"></p>
                            <p id="mount-bed">2</p>
                        </div>
                    </div>
                    <div class="offer">
                        <p>Offer</p>
                        <div class="wifi">
                            <p><img src="/images/wifi.png"></p>
                            <p >Wifi</p>
                        </div>
                        <div class="food">
                            <p><img src="/images/food.png"></p>
                            <p >Breakfast</p>
                        </div>
                        
                    </div>
                    <div class="price">
                        <p>Price Rage</p>
                        <h3 id="price">13$/night</h3>
                    </div>
                </div>
                <div class="button-booking">
                    <button class="button button2" @click="goTo('/payment')">Book Now</button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        methods: {
            goTo(url) {
                console.log(url);
                this.$router.push(url);
                
            }
        },
    }
</script>


Index<style scoped>
    .wrapper-above {
        display: flex;
        margin-left: 7%;
        margin-top:18% ;
    }
    .wrapper-below {
        display: flex;
        justify-content: space-evenly;
        /* margin-left: -17%; */
        margin-top: 2%;
    }
    .description {
        width: 1000px;
        margin-left: 70px;
        /* background-color: bisque; */
    }
    .booking {
        width: 280px;
        height: 546px;
        background-color: rgb(234, 226, 226);
        padding-left: 20px;
        /* margin-left: -15%; */
    }
    .title-wrapper {
        display: flex;
        justify-content: space-between;
    }
    #room {
        color: blue;
    }
    #price {
        color: red;
    }
    .bed {
        display: flex;
    }
    .bed img{
        width: 20px;
        height: 20px;
    }
    #mount-bed {
        margin-left: 7px;
        margin-top: 18px;
    }
    .wifi {
        display: flex;
        margin-top: -10px;
    }
    .wifi img {
        width: 20px;
        height: 20px;
    }
    .food {
        display: flex;
        margin-top: -5px;
    }
    .food img {
        width: 20px;
        height: 20px;
    }


    .search {
        margin-top: 15px;
    }
    #search {
        padding: 0px 5px 25px 50px;
        background-color:  #fff;
    }
    .sub-counter {
        margin-left: 30px;
        /* margin-top: 118%; */
        margin-left: 5%;
        width: 264px;
        height: 434px;
        background-color: aqua;
        
    }
    .wrap-leftcounter {
        margin-left: 15px;
    }
    .wrap-leftcounter hr{
        margin-left: -15px;
    }
    .sub-counter1 {
        /* margin-left: 25px; */
        margin-top: 5%;
        margin-left: 5%;
        width: 264px;
        height: 210px;
        background-color: aqua;
        
    }
    .right-counter {
        margin-top: 1%;
        margin-left: 2%;
        width: 1155px;
    }


   .grid-container {
        display: grid;
        gap: 10px;
        /* background-color: #2196F3; */
        /* padding: 10px; */
        
    }

    .grid-item {
        background-color: rgba(255, 255, 255, 0.8);
        text-align: center;
        /* padding: 20px;  */
        font-size: 30px;
        
    }

    .item1 {
        grid-column: 1 ;
        grid-row: 1;
    }

    .item1 img {
        width: 100%;
        height: 100%;
        object-fit: cover;
    }
    .item2 img {
        width: 100%;
        height: 100%;
        object-fit: cover;
    }
    .item3 img {
        width: 100%;
        height: 100%;
        object-fit: cover;
    }
    .item5 img {
        width: 32.8%;
        height: 100%;
        object-fit: cover;
    }


    .item2 {
        grid-column: 2 /span 2 ;
        grid-row: 1 / span 2;
    }
    .item5 {
        grid-column: 1 / span 3;
        grid-row: 3;
    }


    .button {
  background-color: rgb(242, 0, 0); /* Green */
  border: none;
  color: white;
  padding: 15px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 20px;
  width: 260px;
  margin-top: 20px;
  cursor: pointer;
  -webkit-transition-duration: 0.4s; /* Safari */
  transition-duration: 0.4s;
}
.button2:hover {
  box-shadow: 0 12px 16px 0 rgba(0,0,0,0.24),0 17px 50px 0 rgba(0,0,0,0.19);
}
</style>