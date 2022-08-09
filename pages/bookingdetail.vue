<template>
    <div class="wrapper">
        <div class="title">
            <div class="icon">
                <img src="/images/iconcheck.png"/>
            </div>
            <div class="booking-success">
                <h1>Booking Success</h1>
            </div>
        </div>
        <center>
            <h3>Booking Detail</h3>
        </center>
        <div class="booking-detail">
            <div class="caption">
                <p>Phonenumber:</p>
                <p>Hotel:</p>
                <p>Location:</p>
                <p>Check-in:</p>
                <p>Cheeck-out:</p>
                <p>Price:</p>
                <p>Payment:</p>
            </div>
            <div class="description">
                <P>099555460</P>
                <P>Delux Hotel</P>
                <P>Phnom Penh</P>
                <P>Jul, 04, 2022</P>
                <P>Jul, 06, 2022</P>
                <P>13$/night</P>
                <P>Cash</P>
            </div>
        </div>
        <center>
            <img src="/images/qrcode.png">
            <div class="button">
                <button id="save">Save</button>
                <button id="done" @click="goTo('/provinces/room/roomdetail1')">Done</button>
        </div>
        </center>
        
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

<style scoped>
.wrapper {
    width: 850px;
    height: 518px;
    background-color: rgb(214, 213, 213);
}
.title {
    display: flex;
    margin-top: 320px;

}
.wrapper img {
    width: 100px;
    height: 100px;

}
.booking-success {
    margin-top: 10px;
}
.booking-detail {
    display: flex;
}
.button {
    margin-top: 20px;

}
.button #save {
    padding: 15px 50px 15px 50px;
    background-color: red;
    color: white;
    border: 1px;
    border-radius:10px 0px 0px 10px;
 }
 .button #done {
    padding: 15px 50px 15px 50px;
    background-color: red;
    color: white;
    border: 1px;
    border-radius: 0px 10px 10px 0px;
 }

</style>