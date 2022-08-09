<template>
    <div class="wrapper">
        <div class="back-arrow">
                <img src="/images/back-arrow.webp">
                <h2 @click="goTo('/')"></h2>
        </div>
        <div class="origin">
            <img id="location" src="/images/location-icon.png">
            <input class="inp" placeholder="Chose Origin"/>
        </div>
        <div class="departure">
            <img id="location" src="/images/location-icon.png">
            <input class="inp" placeholder="Choose Departure"/>
        </div>
        <p>Departure Date</p>
        <input class="inp" type="date" placeholder="Check-Out" />
    </div>
</template>

<script>
    export default {
      methods: {
        goTo(url) {
            console.log(url)
            this.$router.push(url)
            
        }
      },  
    }
</script>

<style scoped>
.wrapper {
    margin-top: 320px;
    margin-left: 130px;
    font: 20px;
}
.inp {
    border:none;
    border-bottom: 1px solid #1890ff;
    padding: 5px 10px;
    outline: none;
 }

[placeholder]:focus::-webkit-input-placeholder {
    transition: text-indent 0.4s 0.4s ease; 
    text-indent: -100%;
    opacity: 1;
 }
 #location {
    width: 20px;
 }
 .back-arrow {
    display: flex;
    
 }
.back-arrow img {
    width: 30px;
    height:30px;
    margin-top: 20px;
    margin-right: 10px;
}

</style>