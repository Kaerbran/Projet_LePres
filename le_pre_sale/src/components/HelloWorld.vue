<template>
  <div>
    <div class="main">
      <picture class="pictures">
        <img class="pictures__img" src="../assets/3_Affiche_PreSale.jpg" alt="Affiche du festival de musique, Le Pré Salé">
      </picture>
      <div class="timer">
        <p class="timer__p">Le Pré Salé commence dans :</p>
        <div id="timer" class="timer_clock">
          <!--  Timer Component  -->
          <CountDown 
            starttime="June 24, 2022 18:00:00" 
            endtime="June 24, 2022 23:59:59" 
            trans='{  
            "day":"Jours",
            "hours":"Heures",
            "minutes":"Minutes",
            "seconds":"Secondes",
            "expired":"Event has been expired.",
            "running":"Till the end of event.",
            "upcoming":"Till start of event.",
            "status": {
            "expired":"Expired",
            "running":"Running",
            "upcoming":"Future"
            }}'
          ></CountDown>
          <!--  End! Timer Component  -->
        </div>
        
        <button class="timer__btt" onclick="location.href='https://my.weezevent.com/les-pres-sales';">
          Billeterie <br>
          <em>10€/pers.</em>
        </button>

        <div class="ContainerBTT">
          <img class="ContainerBTT__img ContainerBTT__img--left" src="../assets/social/facebook.png" onclick="location.href='https://www.facebook.com/PresSalesFestival/';" />
          <img class="ContainerBTT__img ContainerBTT__img--right" src="../assets/social/instagram.png" onclick="location.href='https://www.instagram.com/festival_pres_sales/';" />
          <img class="ContainerBTT__img ContainerBTT__img--right" src="../assets/social/youtube.png" onclick="location.href='https://www.youtube.com/channel/UCRCo48bidvz4M6rO5sgFpTQ';" />
        </div>
        
      </div>
    </div>

    <LaProgrammation />
    <LesAnimations />
    <LesSponsors />
    <LeLieux />
  </div>
</template>

<script>
import LaProgrammation from "../components/LaProgrammtion"
import LesAnimations from "../components/LesAnimations"
import LeLieux from "../components/LeLieux"
import CountDown from "../components/CountDown"
import LesSponsors from "../components/LesSponsors"



export default {
  name: 'HelloWorld',
  components: {
    LaProgrammation,
    LesAnimations,
    LeLieux,
    CountDown,
    LesSponsors
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
*, *:before, *:after {
  box-sizing: border-box;
  margin: 0px 0px 0px 0px ; // top right bottom left
}

//adding the new font
@font-face {
    font-family: Berlin;
    src: url('../assets/fonts/Berlin Sans FB Regular.ttf');
}

//mixin afin de pouvoir inclure des media dans sass
@mixin media-device-max($_max-device-width){
    @media screen and (max-device-width: $_max-device-width){
        &{ @content; }
    }
}

.main {
  display: flex;
  justify-content: center;

  position: relative;
  width: auto; height: 130vh;

  @include media-device-max(900px){
      flex-direction: column;
      height: 90vh;
  }
  
  @include media-device-max(670px){
      flex-direction: column;
      height: 125vh;
  }

  &:before{
    content: "";    
    background-image: url("../assets/P1020229 1.JPG");
    background-color: #cccccc; /* Used if the image is unavailable */
    filter: brightness(1.7);

    position: absolute;
    top: 0; left: 0; right: 0;
    z-index: -1;

    display: block; 
    background-size:cover;
    width: 100%; height: 100%;
  }
}

.pictures{
  margin: auto 0px auto 0px ; // top right bottom left
  @include media-device-max(900px){
    margin: 10px auto 0 auto ; // top right bottom left
  }
  &__img{
    width: 100%; max-width: 600px;
    border-radius: 10%;

    object-fit: contain;
  }
}

.timer{
  height: 200px;
  margin: auto 0px auto 30px ; // top right bottom left

  display: flex;
  justify-content: center; flex-direction: column;

  &__p{
    margin: 0px auto 20px auto ; // top right bottom left
    font-size: 15px;
    font-family:'Berlin'; //font-size: 1em;
    font-weight: 600;
    text-align: center;
    color: white;
    padding: 0px 5px 0px 5px ; // top right bottom left
  }
  &__clock{

  }
  &__btt{
    margin: 30px auto 0px auto ; // top right bottom left
    padding: 0.7em 1.4em;
    display:inline-block;

    border-radius:0.15em;
    box-sizing: border-box;

    text-decoration:none;
    font-family:'Berlin';
    text-transform:uppercase;
    font-weight:400; 
    color:#FFFFFF;

    background: rgb(56,116,69);
    background: linear-gradient(0deg, rgba(56,116,69,1) 0%, rgba(253,187,45,1) 100%);
    //background-color:rgba(204, 96, 63, 1);

    box-shadow:inset 0 -0.6em 0 -0.35em rgba(0,0,0,0.17);
    text-align:center;
    position:relative;

    &:hover{
      cursor: pointer;
    }

    font-size: 3vw;
    @include media-device-max(900px){
        font-size: 1em;
    }
  }
}

em{
  text-transform: none;
  font-size: 16px;
}

.ContainerBTT{
  display: flex;
  margin: 10px auto 0px auto ; // top right bottom left

  &__img{
    width: 50px;

    &:hover{
      cursor: pointer;
    }

    &--left{
      margin: 0px 10px 0px 0px ; // top right bottom left
    }
    &--right{
      margin: 0px 0px 0px 10px ; // top right bottom left
    }
  }
}
</style>
