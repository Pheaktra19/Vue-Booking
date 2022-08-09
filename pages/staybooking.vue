<template>
    <div>
        
        <div class="header">
            <div class="title">
                <p>Welcome</p>
                <h2>Pheaktra</h2>
            </div>
            <div class="picture">
                <img src="/images/stay.png">
            </div>
        </div>

        <div >
            <form class="wrapper">
                <div class="location">
                    <i class="fa fa-map-marker" aria-hidden="true"></i>
                    <select name="cars" id="cars">
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
                <div class="check-in">
                    <!-- <i class="fa fa-calendar" aria-hidden="true"></i> -->
                <input type="date" placeholder="Check-In" name="usrnm">
                </div>            
                <div class="check-out">
                    <!-- <i class="fa fa-calendar" aria-hidden="true"></i> -->
                    <input type="date" placeholder="Check-Out" name="usrnm">
                </div>
            </form>
        </div>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>
.header {
    margin-top: 18%;
    display: flex;
    justify-content: center;
    align-content: center;
    width: 100%;
    height: 40vh;
    background-color: pink;
}
.title {
    margin: 100px 0px 0px 0px;
    color: #fff;
}
img {
    margin-left: 200px;
    width: 300px;
    height: 300px;
    /* background-color: gray; */
}
.picture {
    margin-left: 50px;
    padding: 20px 100px 20px 0px;
    width: 500px;
    height: 300px;
    border-radius: 20px;
    background-color: gray;
}
.wrapper {
    /* margin-top: 10%; */
    display: flex;
}
.check-in {
    padding: 15px 5px 5px 5px;
    margin-left: 60px;
}
.check-out {
    margin-left: 60px;
}
</style>