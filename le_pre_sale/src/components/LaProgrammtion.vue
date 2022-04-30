<template>
  <div class="container"> 
      <h2 class="container__h2">La Programmation:</h2>
      <div class="container__div">
          <h3 class="container__h3">Thibault Sibella <br>(WildPoP / Funk)</h3>
          <picture class="container__picture">
              <img class="container__picture__img" src="../assets/Thibaut-sibella-Groupe.jpg" alt="">
          </picture>
          <p class="container__p">Thibaut Sibella and the Graveyard Shift proposent des compositions originales folk pleines de mélodies et d’émotions à travers laquelle ils dépeignent des histoires, des rencontres, des souvenirs. Une guitare, un banjo, une contre basse et trois voix au service d’une musique inspirée par la folk bluegrass/indie et le rock des années 60 qui se veux pleine de bonnes vibrations.</p>
      </div>
      <div class="container__div">
          <h3 class="container__h3">Dudes Of Groove Society<br>(New Funk)</h3>
          <picture class="container__picture">
              <img class="container__picture__img" src="../assets/DOGS.png" alt="">
          </picture>
          <p class="container__p">Le groupe préfère définir son style en “New Funk – Hip-Hop” et ne s’embête pas pour mélanger l’éléctro et les musiques actuelles avec la funk de James Brown, ce qu’il en ressort c’est une énergie folle et un show carré au possible !</p>
      </div>
      <div class="container__div">
          <h3 class="container__h3">Tadeo<br>(GROOVE / Hip Hop)</h3>
          <picture class="container__picture">
              <img class="container__picture__img" src="../assets/Tadeos.jpeg" alt="">
          </picture>
          <p class="container__p">Une envolée de mots posés sur un groove de base Hip Hop. Les textes sentent le bon vin et s'appuient sur des sonorités swing ou funk permettant le déhanchement et la danse !</p>
      </div>
  </div>
</template>

<script>
export default {
  name: 'LaProgrammation'
}
</script>

<style scoped lang="scss">
*, *:before, *:after {
  box-sizing: border-box;
  margin: 0px 0px 0px 0px ; // top right bottom left
}

@mixin media-device-max($_max-device-width){
    @media screen and (max-device-width: $_max-device-width){
        &{ @content; }
    }
}

.container{
display: flex;
flex-wrap: wrap;
justify-content: space-around;

    &__h2{
        display: inline-block;
        width: 100vw;

        text-align: center;
        font-family:'Monoton',sans-serif; font-size: 1.5em;
        font-weight: 400;
        color: rgba(204, 96, 63, 1);

        margin: 30px 0px 30px 0px ; // top right bottom left
        padding: 0px 0px 0px 0px ; // top right bottom left

        &::before, &::after{
            content: "";
            background: rgba(204, 96, 63, 1);
            display: block;
            height: 2px;
            margin: 15px 0px 15px 0px ; // top right bottom left

        }

    }
    &__div{
        width: 400px;

        margin: 0px 0px 0px 0px ; // top right bottom left
        padding: 0px 0px 0px 0px ; // top right bottom left

        @include media-device-max(900px){
            width: 150px
        }
    }
    &__h3{
        font-family:'Monoton',sans-serif; font-size: 1em;
        font-weight: 400;
        text-align: center;
    }
    &__picture{        
        &__img{
            width: 100%;
            object-fit: contain;
            padding: 5px 0px 5px 0px ; // top right bottom left
        }
    }
    &__p{
        font-family:'Share',sans-serif; font-size: 1em;
        font-weight: 400;
        padding: 5px 0px 5px 0px ; // top right bottom left
    }
}

</style>
