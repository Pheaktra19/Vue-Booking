<template>
    <div class="wrapper">
        <div class="grid-container">
            <div class="grid-item">
                <h3>Booking Cambodia</h3>
                <p id="title">Explore the world with Booking.com. Big savings on homes, hotels, flights, car rentals, taxis, and attractions – build your perfect trip on any budget. Whether you’re looking for hotels, homes.</p>
                <div class="grid-followus">
                    <div class="grid-item1">
                        <img id="facebook" src="/images/fbicon.webp">
                    </div>
                    <div class="grid-item1">
                        <img id="tiktok" src="/images/tiktokicon.png">
                    </div>
                    <div class="grid-item1">
                        <img id="ig" src="/images/igicon.webp">
                    </div>
                    <div class="grid-item1">
                        <img id="youtube" src="/images/youtubeicon.webp">
                    </div>      
                </div>
            </div>
            <div class="grid-item">
                <h3>Navigation</h3>
                <p>Stay Booking</p>
                <p>Food Booking</p>
                <p>Fly Booking</p>
                <p>Cars Booking</p>
                <p>Other Services</p>
            </div>
            <div class="grid-item">
                <h3>Contact</h3>
                <div class="telephone">
                    <p><img src="/images/cellcard1.jpg"/></p>
                    <p id="phone">092200661</p>
                </div>
                <p>Email: Bookingcambodia@gmail.com</p>
            <span>
                Address: #95, st 164 (Baktouk School) 
                Phnom Penh, Cambodia
            </span>
            </div> 
            <div class="grid-item">
                <h3>Download App</h3>
                <img id="app-store" src="/images/app-store.png">
                <img id="play-store" src="/images/play-store.png">
            </div> 
        </div>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>
.wrapper {
    height: 35vh;
    padding-left: 140px;
    padding-right: 100px;
    background-color: gray;
    overflow: hidden;
}

.grid-container {
  display: grid;
  grid-template-columns: minmax(200px, 400px) minmax(200px,200px) minmax(200px, 400px) minmax(200px, 400px);
}
.grid-item {
  /* padding: 20px; */
  font-size: 20px;
  text-align: left;
}
#title {
    padding-right: 55px;
}
.telephone {
    display: flex;
    
}
.telephone img {
    width: 30px;
    height: 30px;
}
.telephone #phone {
    margin-left: 10px;
}
.grid-item #app-store {
    margin-left: -40px;
    width: 250px;
    height: 100px;
}
.grid-item #play-store {
    width: 200px;
    height: 75px;
}

.grid-followus {
  display: grid;
  grid-template-columns: minmax(20px, 40px) minmax(20px, 40px) minmax(20px, 40px) minmax(20px, 40px);  
  
}
.grid-item1 img {
    width: 40px;
    height: 40px;
    background-color: white;
}
#tiktok {
   /* margin-top: 5px; */
   height: 35px;
   margin-left: 10px;
   padding-bottom: 3px;
}
#ig {
    /* margin-top: 4px; */
    height: 35px;
    margin-left: 20px;
    padding-bottom: 3px;

}
#youtube {
    margin-left: 30px;
}


</style>