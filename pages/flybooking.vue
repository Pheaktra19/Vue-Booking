<template>
    <div class="wrapper">
        <H1>Booking Fly</H1>
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

</style>