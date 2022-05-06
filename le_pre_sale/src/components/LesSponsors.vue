<template>
  <div class="container">
    <h2 class="container__h2">Nos Partenaires :</h2>
    <div class="container__div">
        <h3 class="container__h3"></h3>
        <picture class="container__picture">
            <img class="container__picture__img" src="../assets/LOGO_CYNNOTEK.png" alt="Logo de l'entreprise Cynnotek">
        </picture>
        <p class="container__p"></p>
    </div>
    <div class="container__div">
        <h3 class="container__h3"></h3>
        <picture class="container__picture">
            <img class="container__picture__img" src="../assets/LOGO_DOMAINEMURE.jpg" alt="Logo de l'entreprise Projets Julien Bois">
        </picture>
        <p class="container__p"></p>
    </div>
    <div class="container__div">
        <h3 class="container__h3"></h3>
        <picture class="container__picture">
            <img class="container__picture__img" src="../assets/LOGO_CROSSFER.png" alt="Logo de l'entreprise Projets Julien Bois">
        </picture>
        <p class="container__p"></p>
    </div>
    <div class="container__div">
        <h3 class="container__h3"></h3>
        <picture class="container__picture">
            <img class="container__picture__img" src="../assets/LOGO_JULIENBOIS.jpg" alt="Logo de l'entreprise Projets Julien Bois">
        </picture>
        <p class="container__p"></p>
    </div>
    <div class="container__div">
        <h3 class="container__h3"></h3>
        <picture class="container__picture">
            <img class="container__picture__img" src="../assets/LOGO_MAKITA.png" alt="Logo de l'entreprise Makita">
        </picture>
        <p class="container__p"></p>
    </div>
    <div class="container__div">
        <h3 class="container__h3"></h3>
        <picture class="container__picture">
            <img class="container__picture__img" src="../assets/LOGO_DIAM.jpeg" alt="Logo de l'entreprise Noumatrouff">
        </picture>
        <p class="container__p"></p>
    </div>
    <div class="container__div">
        <h3 class="container__h3"></h3>
        <picture class="container__picture">
            <img class="container__picture__img" src="../assets/LOGO_cellierMuhlbach.jpg" alt="Logo de l'entreprise Noumatrouff">
        </picture>
        <p class="container__p"></p>
    </div>
    <div class="container__div">
        <h3 class="container__h3"></h3>
        <picture class="container__picture">
            <img class="container__picture__img" src="../assets/LOGO_NOUMATROUFF.png" alt="Logo de l'entreprise Noumatrouff">
        </picture>
        <p class="container__p"></p>
    </div>
    <div class="container__div">
        <h3 class="container__h3"></h3>
        <picture class="container__picture">
            <img class="container__picture__img" src="../assets/LOGO_BERNARD_KOUTNY.jpg" alt="Logo de l'entreprise Bernanrd Koutny">
        </picture>
        <p class="container__p"></p>
    </div>
    <div class="container__div">
        <h3 class="container__h3"></h3>
        <picture class="container__picture">
            <img class="container__picture__img" src="../assets/LOGO_SourcesSOULTZMATT.jpg" alt="Logo de l'entreprise Sources de Soultzmatt">
        </picture>
        <p class="container__p"></p>
    </div>
    <div class="container__div">
        <h3 class="container__h3"></h3>
        <picture class="container__picture">
            <img class="container__picture__img" src="../assets/LOG_MACK_IMPRESSION.png" alt="Logo de la société Mack Impressions">
        </picture>
        <p class="container__p"></p>
    </div>
    <div class="container__div">
        <h3 class="container__h3"></h3>
        <picture class="container__picture">
            <img class="container__picture__img" src="../assets/LOGO_TTC.jpg" alt="Logo de l'entreprise TTC">
        </picture>
        <p class="container__p"></p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'LesSponsors'
}
</script>

<style scoped lang="scss">
//import des polices d'écritures
@import url('https://fonts.googleapis.com/css2?family=Monoton&family=Share&display=swap');

//mixin afin de pouvoir inclure des media dans sass
@mixin media-device-max($_max-device-width){
    @media screen and (max-device-width: $_max-device-width){
        &{ @content; }
    }
}

*, *:before, *:after {
  box-sizing: border-box;
  margin: 0px 0px 0px 0px ; // top right bottom left
}

.container{
display: flex;
flex-wrap: wrap;
justify-content: flex-start;

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
        width: 150px;

        margin: 0px 0px 10px 0px ; // top right bottom left
        padding: 0px 0px 0px 0px ; // top right bottom left
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

    }
}

</style>
