<template>
  <div>
    <NavSite />

    <div class="main">
      <picture class="pictures">
        <img class="pictures__img" src="../assets/Affiche_découpe.jpg" alt="">
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
        <button class="timer__btt">
          Billeterie
        </button>
      </div>
    </div>

    <LaProgrammation />
    <LesAnimations />
    <LeLieux />
  </div>
</template>

<script>
import NavSite from "../components/NavSite"
import LaProgrammation from "../components/LaProgrammtion"
import LesAnimations from "../components/LesAnimations"
import LeLieux from "../components/LeLieux"
import CountDown from "../components/CountDown"

export default {
  name: 'HelloWorld',
  components: {
    NavSite,
    LaProgrammation,
    LesAnimations,
    LeLieux,
    CountDown
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
*, *:before, *:after {
  box-sizing: border-box;
  margin: 0px 0px 0px 0px ; // top right bottom left
}

.main {
  display: flex;
  justify-content: center;

  //overflow: auto;
  position: relative;

  width: auto; height: 90vh;

  //background-image: url("../assets/P1020229 1.JPG");
  //background-color: #cccccc; /* Used if the image is unavailable */
  //background-size: cover;
  //filter: saturate(100%);
  //filter: brightness(1.5);
  //height
  
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
    width: 110%; height: 110%;
  }
}

.pictures{
  margin: auto 0px auto 0px ; // top right bottom left
  
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
    font-family:'Monoton',sans-serif;
    text-transform:uppercase;
    font-weight:400; font-size: 1.5em;
    color:#FFFFFF;
    background-color:rgba(204, 96, 63, 1);

    box-shadow:inset 0 -0.6em 0 -0.35em rgba(0,0,0,0.17);
    text-align:center;
    position:relative;
  }
}


</style>
