<template>
<div class="wrapper">
    <div class="popup" id="popup-1">
        <div class="overlay"></div>
        <div class="content">
            <h1>Note</h1>
            <p>Booking will be canceled id payment is not received before 12:00 AM on the day of check-in.</p>
            <hr/>
            <button @click="goTo('/bookingdetail')">Confirm</button>
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

<style scoped>
     
     .wrapper {
        margin-top: 320px;
     }

    .popup .overlay{
         position:fixed;
         top:0px;
         left:0px;
         width:100vw;
         height:100vh;background:rgba(0,0,0,0.7);
         z-index:1;
         display: block;
    }
 

    .popup .content{
        position:absolute;
        top:50%;
        left:50%;
        transform:translate(-50%,-50%);
        background:#fff;
        width:450px;
        height:220px;
        z-index:2;
        text-align:center;
        padding:20px;
        box-sizing:border-box;
        display: block;
         transition:all 300ms ease-in-out;
        transform:translate(-50%,-50%)scale(1);
    }

    
</style>