<template>
    <div class="wrapper">
        <div class="back-arrow">
                <img src="/images/back-arrow.webp">
                <h2 @click="goTo('/')">Home</h2>
        </div>
        <div class="tab">
            <button @click="selectTab('oneway')" class="oneway tab-active">One Way</button>
            <button @click="selectTab('roundtrip')" class="roundtrip" >Round Trip</button>
        </div>
        <br/>
        <div v-if="currentTab=='oneway'" id="London" class="tabcontent">
            <div class="origin">
                <img id="location" src="/images/location-icon.png">
                <input class="inp" placeholder="Chose Origin"/>
            </div>
                <div class="departure">
                <img id="location" src="/images/location-icon.png">
            <input class="inp" placeholder="Choose Departure"/>
            </div>
            <h3>Departure Date</h3>
            <input class="inp" type="date" placeholder="Check-Out" />


        </div>

        <div v-else id="Paris" class="tabcontent">
            <div class="origin">
                <img id="location" src="/images/location-icon.png">
                <input class="inp" placeholder="Chose Origin"/>
            </div>
                <div class="departure">
                <img id="location" src="/images/location-icon.png">
            <input class="inp" placeholder="Choose Departure"/>
            </div>
            <div class="date">
                <div class="departure-date">
                    <h3>Departure Date</h3>
                    <input class="inp" type="date" placeholder="Check-Out" />
                </div>
                <div class="return-date">
                    <h3>Return Date</h3>
                    <input class="inp" type="date" placeholder="Check-Out" />
                </div>
            </div>
        </div>
</div>
</template>

<script>
    export default {
        data() {
            return {
                currentTab: "oneway"
            }
        },
        methods: {
            goTo(url) {
                console.log(url)
                this.$router.push(url)
                
            },

            selectTab(tab){
                this.currentTab=tab
                if(tab == 'oneway') {
                    document.querySelector('.oneway').classList.add('tab-active')
                    document.querySelector('.roundtrip').classList.remove('tab-active')

                } else {
                  document.querySelector('.roundtrip').classList.add('tab-active')
                  document.querySelector('.oneway').classList.remove('tab-active')

                }
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
 .direction {
    display: flex;
    
 }
 .round-trip {
    margin-left: 70px;
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

/* Create an active/current tablink class */
.tab-active {
  color:red;
   border:none;
    border-bottom: 2px solid red;
    padding: 5px 10px;
    outline: none;
}
.date {
    display: flex;

}
.return-date {
    margin-left: 50px;
}


</style>