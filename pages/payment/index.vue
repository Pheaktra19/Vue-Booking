<template>
    <div class="wrapper">

        
            <div class="back-arrow">
                <img src="/images/back-arrow.webp">
                <h2 @click="$router.go(-1)">Roomdetail</h2>
            </div>
        <div class="sub-wrapper">
            <p>Contact Information *</p>
            <div class="contact-info">
                <div class="name">
                    <input class="inp" placeholder="Kong Sopheaktra"/>
                </div>
                <div class="phone">
                    <input class="inp" placeholder="+85599555460"/>
                </div>
            </div>
            <h1>booking Information</h1>

            <div class="booking-information">
                <div class="booking-type">
                    <h3>Booking Type:</h3>
                    <h3>Location:</h3>
                    <h3>Hotel:</h3>
                    <h3>Check-in Date:</h3>
                    <h3>Check-out Date:</h3>
                    <h3>Price Rage:</h3>
                </div>
                <div class="booking-description">
                    <h3 id="description">Stay</h3>
                    <h3 id="description">Phnom Penh</h3>
                    <h3 id="description">Delux Hotel</h3>
                    <h3 id="description">Jan, 04, 2022</h3>
                    <h3 id="description">Jan, 06, 2022</h3>
                    <h3 id="price">13$/night</h3>
                </div>
            </div>
            <h1>Payment</h1>
            <div class="payment-method">
                <div class="payment-text">
                    <p id="payment-method">Choose Your Payment Method:</p>
                </div>
                 <div class="card">
                <label class="container">
                    <input   type="radio" checked="checked" name="radio">
                    <span class="checkmark"></span>
                    <img src="/images/wallet.png">
                </label>
                <label class="container">
                    <input type="radio" name="radio">
                    <span class="checkmark"></span>
                    <img src="/images/aba.jpg">
                </label>
                <label class="container">
                    <input type="radio" name="radio">
                    <span class="checkmark"></span>
                    <img src="/images/wing.jpg">
                </label>
            </div>
            </div>
           
            <div class="button">
                <button id="cancel">Cancel</button>
                <button id="confirm" @click="displayPopup">Confirm</button>
            </div>
        </div>

         <ThePopup v-if="showPopup"></ThePopup>
        
    </div>
</template>

<script>
import ThePopup from '~/components/ThePopup.vue';
    export default {
    data() {
        return {
            items: [
                {
                    url: "/provinces/room/roomdetail1"
                }
            ],

            showPopup: false
        };
    },
    
    created () {
        this.$nuxt.$on('close-popup', () => {
            this.showPopup = false
        })
    },
    
    beforeDestroy () {
        this.$nuxt.$off('close-popup')
    },


    methods: {
        goTo(url) {
            console.log(url);
            this.$router.push(url);
        },

        displayPopup(){
            this.showPopup = true
        },

        closePopup(){
            this.showPopup = false
        }

    },
    components: { ThePopup }
}
</script>

<style scoped>
.wrapper {
    margin-top: 18.8%;
    width: 1000px;
    height: 700px;
    /* background-color: aquamarine; */
}
.sub-wrapper {
    margin-left:50%;
}
.contact-info {
    display: flex;
    /* justify-content: space-evenly; */
}
.back-arrow {
    display: flex;
    margin-left: 14%;
}
.back-arrow img {
    width: 30px;
    height:30px;
    margin-top: 20px;
    margin-right: 10px;
}
.booking-information {
    display: flex;
}
.booking-description {
    margin-left: 140px;
}
#description {
    color: blue;
}
#price {
    color: red;
}
.payment-method {
    display: flex;
}
#payment-method {
    margin-top: 72px;
}
.container {
  display: block;
  position: relative;
  padding-left: 35px;
  margin-bottom: 12px;
  cursor: pointer;
  font-size: 22px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
/* The container */
.container {
  margin-left: 70px;
  display: block;
  position: relative;
  padding-left: 35px;
  margin-bottom: 12px;
  cursor: pointer;
  font-size: 22px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

/* Hide the browser's default radio button */
.container input {
  position: absolute;
  opacity: 0;
  cursor: pointer;
}

/* Create a custom radio button */
.checkmark {
  position: absolute;
  top: 0;
  left: 0;
  height: 25px;
  width: 25px;
  background-color: #eee;
  border-radius: 50%;
}

/* On mouse-over, add a grey background color */
.container:hover input ~ .checkmark {
  background-color: #ccc;
}

/* When the radio button is checked, add a blue background */
.container input:checked ~ .checkmark {
  background-color: #2196F3;
}

/* Create the indicator (the dot/circle - hidden when not checked) */
.checkmark:after {
  content: "";
  position: absolute;
  display: none;
}

/* Show the indicator (dot/circle) when checked */
.container input:checked ~ .checkmark:after {
  display: block;
}

/* Style the indicator (dot/circle) */
.container .checkmark:after {
 	top: 9px;
	left: 9px;
	width: 8px;
	height: 8px;
	border-radius: 50%;
	background: white;
}
.container img {
    width: 50px;
    height: 50px;
}
.payment-method {
    display: flex;
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
 .phone {
    margin-left: 20px;

 }
 .button #cancel {
    padding: 10px 45px 10px 45px;
    background-color: red;
    color: white;
 }
 .button #confirm {
    padding: 10px 45px 10px 45px;
    background-color: blue;
    color: white;
 }
</style>
