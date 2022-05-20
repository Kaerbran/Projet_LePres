<template>
  <div class="container">
    <h2 class="container__h2">Nos Partenaires :</h2>
    <div>
        <div class="container__div">
            <picture class="container__picture">
                <img class="container__picture__img container__picture__img--hover" src="../assets/LOGO_CYNNOTEK.png" alt="Logo de l'entreprise Cynnotek" onclick="location.href='https://www.cynnotek.fr/';" >
            </picture>
        </div>
        <div class="container__div">
            <picture class="container__picture">
                <img class="container__picture__img container__picture__img--marge container__picture__img--hover" src="../assets/LOGO_CROSSFER.png" alt="Logo de l'entreprise Projets Julien Bois" onclick="location.href='https://www.crossferfrance.fr/';">
            </picture>
        </div>
    </div>
    <div class="container__div">
        <picture class="container__picture">
            <img class="container__picture__img container__picture__img--hover" src="../assets/LOGO_DOMAINEMURE.jpg" alt="Logo de l'entreprise Projets Julien Bois" onclick="location.href='https://www.mure.com/';" >
        </picture>
    </div>
    <div class="container__div">
        <picture class="container__picture">
            <img class="container__picture__img" src="../assets/LOGO_JULIENBOIS.jpg" alt="Logo de l'entreprise Projets Julien Bois">
        </picture>
    </div>
    <div>
        <div class="container__div">
            <picture class="container__picture">
                <img class="container__picture__img container__picture__img--hover" src="../assets/LOGO_MAKITA.png" alt="Logo de l'entreprise Makita" onclick="location.href='https://www.remymuller.fr/';">
            </picture>
        </div>
        <div class="container__div">
            <picture class="container__picture">
                <img class="container__picture__img container__picture__img--marge container__picture__img--hover" src="../assets/LOGO_SourcesSOULTZMATT.jpg" alt="Logo de l'entreprise Sources de Soultzmatt" onclick="location.href='http://www.lisbeth.fr/';"> 
            </picture>
        </div>
    </div>
    <div class="container__div">
        <picture class="container__picture">
            <img class="container__picture__img container__picture__img--hover" src="../assets/LOGO_DIAM.jpeg" alt="Logo de l'entreprise Noumatrouff" onclick="location.href='https://www.diam-bouchon-liege.com/';">
        </picture>
    </div>
    <div>
        <div class="container__div">
            <picture class="container__picture">
                <img class="container__picture__img container__picture__img--hover container__picture__img--marge" src="../assets/LOGO_cellierMuhlbach.png" alt="Logo de l'entreprise Noumatrouff" onclick="location.href='https://www.noumatrouff.fr/';">
            </picture>
        </div>
        <div class="container__div">
            <picture class="container__picture">
                <img class="container__picture__img container__picture__img--hover container__picture__img--marge" src="../assets/LOGO_MeilleurTaux.png" alt="Logo de l'entreprise française meilleur taux" onclick="location.href='http://www.meilleurtaux.com/';">
            </picture>
        </div>
        <div class="container__div">
        <picture class="container__picture">
            <img class="container__picture__img container__picture__img--marge" src="../assets/LOGO_Henninger.jpg" alt="Logo de l'entreprise Henninger">
        </picture>
    </div>
    </div>
    <div class="container__div">
        <picture class="container__picture">
            <img class="container__picture__img" src="../assets/LOGO_NOUMATROUFF.png" alt="Logo de l'entreprise Noumatrouff">
        </picture>
    </div>
    <div>
        <div class="container__div">
            <picture class="container__picture">
                <img class="container__picture__img container__picture__img--marge" src="../assets/LOGO_BERNARD_KOUTNY2.jpg" alt="Logo de l'entreprise Bernanrd Koutny">
            </picture>
        </div>
        <div class="container__div">
            <picture class="container__picture">
                <img class="container__picture__img container__picture__img--hover container__picture__img--marge" src="../assets/LOGO_CAPVISION.png" alt="Logo de l'entreprise Capvision" onclick="location.href='http://www.capvision.fr/';">
            </picture>
        </div>
    </div>
    <div class="container__div">
        <picture class="container__picture">
            <img class="container__picture__img container__picture__img--hover" src="../assets/LOG_MACK_IMPRESSION.png" alt="Logo de la société Mack Impressions" onclick="location.href='https://www.imprimerie-mack.com/';">
        </picture>
    </div>
    <div class="container__div">
        <picture class="container__picture">
            <img class="container__picture__img container__picture__img--hover" src="../assets/LOGO_TTC.jpg" alt="Logo de l'entreprise TTC" onclick="location.href='https://www.tt-chauffage.com/';">
        </picture>
    </div>
    <div class="container__div">
        <picture class="container__picture">
            <img class="container__picture__img" src="../assets/LOGO_AQUATEC.png" alt="Logo de l'entreprise Aquatec">
        </picture>
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

@include media-device-max(900px){
    justify-content: space-around;
}

background: rgb(252,176,69);
background: linear-gradient(190deg, rgba(131,58,180,1) 20%, rgba(253,29,29,1) 54%, rgba(252,176,69,1) 100%);

    &__h2{
        display: inline-block;
        width: 100vw;

        text-align: center;
        font-family:'Berlin'; font-size: 3.5vw;
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
        width: 150px;
        margin: 0px 5px 0px 0px ; // top right bottom left
    }
    &__picture{      
        display: flex;
        width:  150px;
        margin: auto 0px auto 0px ; // top right bottom left
        &__img{
            width: 100%;
            background: white;
            object-fit: contain;

            &--marge{
                margin-top: 8px;
            }

            &--hover{
                &:hover{
                    cursor: pointer;
                }
            }
        }
    }
}

</style>
