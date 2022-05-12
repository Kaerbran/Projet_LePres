<template>
  <div class="container"> 
      <h2 class="container__h2">La Programmation:</h2>
      <div class="container__div">
          <h3 class="container__h3">Thibaut Sibella <br>(WildPoP / Funk)</h3>
          <picture class="container__picture">
              <img class="container__picture__img" src="../assets/Thibaut-sibella-Groupe.jpg" alt="Thibaut Sibella et son groupe">
          </picture>
          <p class="container__p">Thibaut Sibella and the Graveyard Shift proposent des compositions originales folk pleines de mélodies et d’émotions à travers laquelle ils dépeignent des histoires, des rencontres, des souvenirs. Une guitare, un banjo, une contre basse et trois voix au service d’une musique inspirée par la folk bluegrass/indie et le rock des années 60 qui se veut pleine de bonnes vibrations.</p>
      </div>
      <div class="container__div">
          <h3 class="container__h3">Dudes Of Groove Society<br>(New Funk)</h3>
          <picture class="container__picture">
              <img class="container__picture__img" src="../assets/DOGS.png" alt="Groupe Dudes of Groove Society">
          </picture>
          <p class="container__p">Le groupe préfère définir son style en “New Funk – Hip-Hop” et ne s’embête pas pour mélanger l’éléctro et les musiques actuelles avec la funk de James Brown, ce qu’il en ressort c’est une énergie folle et un show carré au possible !</p>
      </div>
      <div class="container__div">
          <h3 class="container__h3">Tadeo<br>(GROOVE / Hip Hop)</h3>
          <picture class="container__picture">
              <img class="container__picture__img" src="../assets/Tadeos.jpeg" alt="Groupe Tadeo">
          </picture>
          <p class="container__p">Une envolée de mots posée sur un groove de base Hip Hop. Les textes sentent le bon vin et s'appuient sur des sonorités swing ou funk permettant le déhanchement et la danse !</p>
      </div>
      
      <div class="container__div">
          <h3 class="container__h3">Crucial Rob - Sound System<br>(REGGAE / DUB)</h3>
          <picture class="container__picture">
              <img class="container__picture__img" src="../assets/crucial_rob.jpg" alt="Groupe Crucial Rob">
          </picture>
          <p class="container__p">Nourrit d’univers musicaux et de cultures du monde entier, il est envieux de pouvoir concocter ses propres sonorités, il créé alors le Prophecy Studio. <br>

C’est avec autant d’instruments organiques que de machines et synthétiseurs que Rob créé son univers musical et compose une musique cathartique puissante parfois hypnotique à la rythmique tribale et soutenue. </p>
      </div>
      <div class="container__div">
          <h3 class="container__h3">High Steppa - Sound System<br>(REGGAE / DUB)</h3>
          <picture class="container__picture">
              <img class="container__picture__img" src="../assets/high_rockers.jpg" alt="Groupe High Rockers">
          </picture>
          <p class="container__p">Genève</p>
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
/*
Crucial Rob:Sound System Reggae dub Paris/Orschwihr.

High Rockers :Sound System Reggae dub Genève
*/

.container{
display: flex;
flex-wrap: wrap;
justify-content: space-around;

background: black;

    &__h2{
        display: inline-block;
        width: 100vw;

        text-align: center;
        font-family:'Berlin'; font-size: 3.5vw; //1.5em
        font-weight: 400;
        color: white;

        background: rgb(252,176,69);
        background: linear-gradient(190deg, rgba(131,58,180,1) 20%, rgba(253,29,29,1) 54%, rgba(252,176,69,1) 100%);

        margin: 30px 0px 30px 0px ; // top right bottom left
        padding: 0px 0px 0px 0px ; // top right bottom left

        &::before, &::after{
            content: "";
            background: white;
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
        font-family:'Berlin'; font-size: 1.5vw;
        font-weight: 400; color: white;
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
        font-family:'Berlin'; font-size: 1em;
        font-weight: 400; color: white;
        padding: 5px 0px 5px 0px ; // top right bottom left

        @include media-device-max(900px){
            overflow: auto;
            height: 250px;
        }
    }
}

</style>
