<template>
    <div class="flex">
        <div class="day">
            <span class="number">{{ days }}</span>
            <div class="format">{{ wordString.day }}</div>
        </div>
        <div class="hour">
            <span class="number">{{ hours }}</span>
            <div class="format">{{ wordString.hours }}</div>
        </div>
        <div class="min">
            <span class="number">{{ minutes }}</span>
            <div class="format">{{ wordString.minutes }}</div>
        </div>
        <div class="sec">
            <span class="number">{{ seconds }}</span>
            <div class="format">{{ wordString.seconds }}</div>
        </div>
    </div>
</template>

<script>
export default {

//Code inspired from the below link:
//https://morioh.com/p/1a0af750b8d7

    name: 'CountDown',
    props: ['starttime','endtime','trans'],
    data: function(){
        return{
            timer:"",
            wordString: {},
            start: "",
            end: "",
            interval: "",
            days:"",
            minutes:"",
            hours:"",
            seconds:"",
            message:"",
            statusType:"",
            statusText: "",
        };
    },created: function () {
        this.wordString = JSON.parse(this.trans);
    },
    mounted(){
        this.start = new Date(this.starttime).getTime();
        this.end = new Date(this.endtime).getTime();
        // Update the count down every 1 second
        this.timerCount(this.start,this.end);
        this.interval = setInterval(() => {
        this.timerCount(this.start,this.end);
        }, 1000);
    },
    methods: {
        timerCount: function(start,end){
            // Get todays date and time
            var now = new Date().getTime();

            // Find the distance between now an the count down date
            var distance = start - now;
            var passTime =  end - now;

            if(distance < 0 && passTime < 0){
                this.message = this.wordString.expired;
                this.statusType = "expired";
                this.statusText = this.wordString.status.expired;
                clearInterval(this.interval);
                return;

            }else if(distance < 0 && passTime > 0){
                this.calcTime(passTime);
                this.message = this.wordString.running;
                this.statusType = "running";
                this.statusText = this.wordString.status.running;

            } else if( distance > 0 && passTime > 0 ){
                this.calcTime(distance); 
                this.message = this.wordString.upcoming;
                this.statusType = "upcoming";
                this.statusText = this.wordString.status.upcoming;
            }
        },
        calcTime: function(dist){
            // Time calculations for days, hours, minutes and seconds
            this.days = Math.floor(dist / (1000 * 60 * 60 * 24));
            this.hours = Math.floor((dist % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            this.minutes = Math.floor((dist % (1000 * 60 * 60)) / (1000 * 60));
            this.seconds = Math.floor((dist % (1000 * 60)) / 1000);
        }
    }
}
</script>

<style scoped lang="scss">
//*, *:before, *:after {
//  box-sizing: border-box;
//  margin: 0px 0px 0px 0px ; // top right bottom left
//}

.flex{
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
}

.timer {
    font-size: 20px;
    color: #fff;
    text-align:center;
    margin-top: 50px;

    .day, .hour, .min, .sec {
        font-size: 30px;
        display: inline-block;
        font-weight: 500;
        text-align: center;
        margin: 0 5px;
        .format {
            font-size: 15px;
            font-family:'Share',sans-serif; color: white;
            font-weight: 600;
            opacity: 0.8;
            width: 60px;
            padding: 5px 0px 5px 0px ; // top right bottom left
        }
    }
    .number{
        //background: pink;
        background: rgb(252,176,69);
        background: linear-gradient(190deg, rgba(131,58,180,1) 20%, rgba(253,29,29,1) 54%, rgba(252,176,69,1) 100%);
        padding: 0 5px;
        border-radius: 5px;
        display: inline-block;
        width: 60px;
        text-align: center;
    }
    .message {
        font-size: 14px;
        font-weight: 400;
        margin-top: 5px;
    }

}

</style>
