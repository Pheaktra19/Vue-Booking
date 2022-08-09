<template>
    <div class="wrapper">
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
                    <input id="input" type="date" placeholder="Check-In" name="usrnm"></input>
                </div>
                <p>Check-out date</p>
                <div class="checkout-date">
                    <input id="input" type="date" placeholder="Check-Out" name="usrnm"></input>
                </div>
                <p>Night Stay</p>
                <div class="night-stay">
                    <input id="input" type="date" placeholder="Check-Out" name="usrnm"></input>
                </div>
                <div class="search">
                <form id="search-form" name="search" action="/products" method="get">
                    <input id="search" src="path/to/image" name="search" type="text" value="Search">
                </form>
                </div>
                </div>
            </div>





            <div class="sub-counter1">
                <div class="wrap-leftcounter">
                    <h2 >Filter By:</h2>
                    <hr/>
                    <h3>Star Rating</h3>
                    <form action="/action_page.php">
                        <input type="checkbox" id="vehicle1" name="vehicle1" value="Bike">
                        <label for="vehicle1"> 1 star</label><br>
                        <input type="checkbox" id="vehicle2" name="vehicle2" value="Car">
                        <label for="vehicle2"> 2 stars</label><br>
                        <input type="checkbox" id="vehicle3" name="vehicle3" value="Boat">
                        <label for="vehicle3"> 3 stars</label><br><br>
                        <input type="submit" value="Submit">
                    </form>
                </div>
            </div>
        </div>
        <div class="right-counter">
            <h1 id="properties">Phnom Penh: 15 properties found</h1>
            <div class="picture1" v-for="(item,i) in pictures" :key="i">
                <div class="picture" >
                    <img :src="item.img">
                </div>
                <div class="title">
                    <h1 id="properties">{{ item.name }}</h1>
                    <p id="title"><u>{{item.place }}</u></p>
                    <span>{{item.description }}</span>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
    export default {
       data() {
        return {
            pictures: [
                {
                    img:'/rotanakiri/r1.jpg',
                    name:'Delux Hotel',
                    place:'Daun Penh, Phnom Penh',
                    description:'Centrally located in Phnom Penh, Plantation Urban Resort & Spa is located directly behind the Royal Palace.'
                },

                {
                    img:'/rotanakiri/r2.jpg',
                    name:'The Hotel Phnom Penh',
                    place:'Chomka Morn, Phnom Penh',
                    description:'Centrally located in Phnom Penh, Plantation Urban Resort & Spa is located directly behind the Royal Palace.'
                },
                {
                    img:'/rotanakiri/r3.jpg',
                    name:'The Relaxing Hotel',
                    place:'Beoung Kenh Kong, Phnom Penh',
                    description:'Centrally located in Phnom Penh, Plantation Urban Resort & Spa is located directly behind the Royal Palace.'
                },
                {
                    img:'/rotanakiri/r4.jpg',
                    name:'The-House Questhouse',
                    place:'Beoung Tom Pon, Phnom Penh',
                    description:'Centrally located in Phnom Penh, Plantation Urban Resort & Spa is located directly behind the Royal Palace.'
                },
                {
                    img:'/rotanakiri/r5.jpg',
                    name:'Oakwood Hotel',
                    place:'Royal Place, Phnom Penh',
                    description:'Centrally located in Phnom Penh, Plantation Urban Resort & Spa is located directly behind the Royal Palace.'
                },
                {
                    img:'/phnompenh/intercontenent.jfif',
                    name:'Intercontenent Resort',
                    place:'7 Makara, Phnom Penh',
                    description:'Centrally located in Phnom Penh, Plantation Urban Resort & Spa is located directly behind the Royal Palace.'
                },
                {
                    img:'/phnompenh/meeting.jfif',
                    name:'The Meeting Room Hotel',
                    place:'Toul Kok, Phnom Penh',
                    description:'Centrally located in Phnom Penh, Plantation Urban Resort & Spa is located directly behind the Royal Palace.'
                },
                {
                    img:'/phnompenh/azumaya.jfif',
                    name:'Azumaya Spa and Resort',
                    place:'Dang Kor, Phnom Penh',
                    description:'Centrally located in Phnom Penh, Plantation Urban Resort & Spa is located directly behind the Royal Palace.'
                },
                {
                    img:'/phnompenh/citycenter.jfif',
                    name:'The City Center',
                    place:'Chomka Morn, Phom Penh',
                    description:'Centrally located in Phnom Penh, Plantation Urban Resort & Spa is located directly behind the Royal Palace.'
                },
                {
                    img:'/phnompenh/naki.jfif',
                    name:'Naki Naki Center',
                    place:'7 Makara, Phnom Penh',
                    description:'Centrally located in Phnom Penh, Plantation Urban Resort & Spa is located directly behind the Royal Palace.'
                },
                {
                    img:'/phnompenh/rosewood.jfif',
                    name:'RoseWood Hotel',
                    place:'Toul Kok, Phnom Penh',
                    description:'Centrally located in Phnom Penh, Plantation Urban Resort & Spa is located directly behind the Royal Palace.'
                },
                {
                    img:'/phnompenh/luxeryboutique.jfif',
                    name:'The Luxery Boutique',
                    place:'Beoung Kok, Phnom Penh',
                    description:'Centrally located in Phnom Penh, Plantation Urban Resort & Spa is located directly behind the Royal Palace.'
                },
                {
                    img:'/phnompenh/acomondation.jfif',
                    name:'Acomodation Hotel de Phnom Penh',
                    place:'Mean Chey, Phnom Penh',
                    description:'Centrally located in Phnom Penh, Plantation Urban Resort & Spa is located directly behind the Royal Palace.'
                },
                {
                    img:'/phnompenh/tripatrack.jfif',
                    name:'Trip Track Hotel',
                    place:'Steng Mean Chhey, Phnom Penh',
                    description:'Centrally located in Phnom Penh, Plantation Urban Resort & Spa is located directly behind the Royal Palace.'
                },
                {
                    img:'/phnompenh/pavilion.jfif',
                    name:'Pavilion Hotel',
                    place:'Toul Kok, Phnom Penh',
                    description:'Centrally located in Phnom Penh, Plantation Urban Resort & Spa is located directly behind the Royal Palace.'
                },
            ],
        }
       }, 
    }
</script>

<style scoped>
    .wrapper {
        display: flex;
        margin-left: 7%;
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
        margin-top: 118%;
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
    #properties {
        color: blue;

    }
    #title{
        color: blue;
    }
    
    .left-counter {
        /* display: flex; */
        
    }
    .right-counter {
        margin-top: 19%;
        margin-left: 2%;
        width: 1155px;
        height: 3860px;
        background-color: pink;
    }
    .picture img {
       width: 380px;
       height: 250px;
       background-color: white; 
    }
    .picture1 {
        width: 1150px;
        height: 250px;
        display: flex;
        justify-content: space-between;
        border: 1px solid gray;
    }
</style>