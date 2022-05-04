<template>
  <div class="container"> 
      <h2 class="container__h2">Les Animations:</h2>
      <div class="container__div">
          <h3 class="container__h3">Théo notre jongleur</h3>
          <picture class="container__picture">
              <img class="container__picture__img" src="../assets/Anim1_jongleur.jpg" alt="jongleur de nuit">
          </picture>
          <p class="container__p">Théo est un jongleur de 23 ans venant de Colmar.
Il pratique le jonglage et la manipulation de feu depuis ces 15ans et se présente en spectacle sous le nom de "APoïThéose" dans le but de partager sa passion avec ses spectateurs.
Ouvrez grand vos yeux et profitez bien du spectacle !</p>
      </div>
      <div class="container__div">
          <h3 class="container__h3">The Buvette</h3>
          <picture class="container__picture">
              <img class="container__picture__img" src="../assets/Anim3_buvette.png" alt="buvette dans un festival">
          </picture>
          <p class="container__p">Que serait un bon festival, sans sa buvette!</p>
      </div>
      <div class="container__div">
          <h3 class="container__h3">De la bonne viande</h3>
          <picture class="container__picture">
              <img class="container__picture__img" src="../assets/Anim6_ferme.jpg" alt="agriculteur bovin">
          </picture>
          <p class="container__p">Une belle exploitaion de Bovins et d'Ovins, située à Wintzfelden au fond de la Vallée Noble dans un joli écrin de verdure.</p>
      </div>
      <div class="container__div">
          <h3 class="container__h3">Du vin du Domaine Léon Boesch</h3>
          <picture class="container__picture">
              <img class="container__picture__img" src="../assets/Anim5_LeonBoesch.jpeg" alt="couple de vigneron dans la vigne">
          </picture>
          <p class="container__p">Domaine familiale en production Biodynamique.</p>
      </div>
      <div class="container__div">
          <h3 class="container__h3">Du vin du Domaine Du Clos Saint Landelin</h3>
          <picture class="container__picture">
              <img class="container__picture__img" src="../assets/Anim4_Mure.jpeg" alt="couple de vigneron dans la vigne">
          </picture>
          <p class="container__p">Domaine familiale en production Biodynamique.</p>
      </div>
      <div class="container__div">
          <h3 class="container__h3">Brasserie Taal</h3>
          <picture class="container__picture">
              <img class="container__picture__img" src="../assets/Bierestaal.jpg" alt="l'équipe de la brasserie Taal">
          </picture>
          <p class="container__p">Brasseur de bière artisanale depuis 2017 à Soultzbach-les-Bains.</p>
      </div>
      <div class="container__div">
          <h3 class="container__h3">Earl Sutter</h3>
          <picture class="container__picture">
              <img class="container__picture__img" src="../assets/Sutter.jpg" alt="">
          </picture>
          <p class="container__p">L'Earl Sutter est une exploitation agricole familiale, située à Petit-Landau. On y cultive des légumes bio de saison.</p>
      </div>
  </div>
</template>

<script>
export default {
  name: 'LesAnimations'
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
        width: 300px;

        margin: 0px 0px 10px 0px ; // top right bottom left
        padding: 0px 0px 0px 0px ; // top right bottom left

        @include media-device-max(900px){
            width: 150px
        }
    }
    &__h3{
        font-family:'Monoton',sans-serif; font-size: 1em;
        font-weight: 700;
        text-align: center;
    }
    &__picture{        
        &__img{
            width: 100%;
            //height: 300px;
            object-fit: contain;
            padding: 5px 0px 5px 0px ; // top right bottom left
        }
    }
    &__p{
        font-family:'Share',sans-serif; font-size: 1em;
        font-weight: 400;
        padding: 5px 0px 5px 0px ; // top right bottom left

        @include media-device-max(900px){
            overflow: auto;
            height: 250px;
        }
    }
}

</style>
