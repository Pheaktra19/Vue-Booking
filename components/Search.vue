<template>
    <div class="mmm">
        
        <div class="header">
            
        </div>

        <div >
            <form class="wrapper">
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
                <div class="check-in">
                    <!-- <i class="fa fa-calendar" aria-hidden="true"></i> -->
                <input id="input" type="date" placeholder="Check-In" name="usrnm">
                </div>            
                <div class="check-out">
                    <!-- <i class="fa fa-calendar" aria-hidden="true"></i> -->
                    <input id="input" type="date" placeholder="Check-Out" name="usrnm">
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
.mmm {
    z-index: 999;
    position: fixed;
}

.header {
    /* margin-top: 14.7% ; */
    /* margin: 10.9% ; */
    margin-top: -22%;
    display: flex;
    justify-content: center;
    align-content: center;
    height: 100px;
    /* background-color: pink; */
}

.wrapper {
    /* margin-top: 10%; */
    display: flex;
}
.location {
    margin-left: 13%;
}
.check-in {
    padding: 0px 5px 5px 5px;
    margin-left: 60px;
}
.check-out {
    margin-left: 60px;
}
#input {
    margin-left: -64px;
    padding: 20px 90px 20px 20px ;
    border: 2px solid goldenrod;
}
#select {
    border: 2px solid goldenrod;
    padding: 20px 150px 20px 20px ;
}

</style>