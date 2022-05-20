<template>
  <div class="container">
      <div class="container__presentation">
          Prés salés [pʁe sale]<br>
          (traduction de l'alsacien Sàltz Màtt ou Soultzmatt)<br><br>
          Le Festival Prés Salés c'est quoi?<br><br>
          C'est l'alchimie de sept personnalités habitées par les mêmes passions, guidées par les mêmes convictions. C'est 
          l'envie de partager, par le biais d'un évènement éphémère, l'amour de la musique, des arts et de la culture. De créer
          des liens, de l'échange. Les Prés Salés c'est comme un bon vin qu'on déguste entre copains 
          à refaire le monde un soir d'été. Cette première édition se voudra exclusivement musicale. Elle sera dansante, funk, 
          groove, rock, folk et poétique. Les Prés Salés s'associent avec les acteurs locaux pour vous proposer une restauration 
          faite de produits sains et de qualités.<br>
          Venez éveiller vos sens et régaler vos papilles! 
      </div>
      <h2 class="container__h2">La Programmation:</h2>
      <div class="container__div">
          <h3 class="container__h3">Thibaut Sibella <br>(WildPoP / Funk)</h3>
          <picture class="container__picture">
              <img class="container__picture__img" src="../assets/Thibaut-sibella-Groupe.jpg" alt="Thibaut Sibella et son groupe">
              <img class="container__picture__youtube" src="../assets/social/youtube.png" onclick="location.href='https://www.youtube.com/watch?v=7NjXZ0IffcQ';" />
          </picture>
          <p class="container__p">Thibaut Sibella and the Graveyard Shift proposent des compositions originales folk pleines de mélodies et d’émotions à travers laquelle ils dépeignent des histoires, des rencontres, des souvenirs. Une guitare, un banjo, une contre basse et trois voix au service d’une musique inspirée par la folk bluegrass/indie et le rock des années 60 qui se veut pleine de bonnes vibrations.</p>
      </div>
      <div class="container__div">
          <h3 class="container__h3">Dudes Of Groove Society<br>(New Funk)</h3>
          <picture class="container__picture">
              <img class="container__picture__img" src="../assets/DOGS.png" alt="Groupe Dudes of Groove Society">
              <img class="container__picture__youtube" src="../assets/social/youtube.png" onclick="location.href='https://www.youtube.com/watch?v=I_xf_2gryrE';" />
          </picture>
          <p class="container__p">Le groupe préfère définir son style en “New Funk – Hip-Hop” et ne s’embête pas pour mélanger l’éléctro et les musiques actuelles avec la funk de James Brown, ce qu’il en ressort c’est une énergie folle et un show carré au possible !</p>
      </div>
      <div class="container__div">
          <h3 class="container__h3">Tadeo<br>(GROOVE / Hip Hop)</h3>
          <picture class="container__picture">
              <img class="container__picture__img" src="../assets/Tadeos.jpeg" alt="Groupe Tadeo">
              <img class="container__picture__youtube" src="../assets/social/youtube.png" onclick="location.href='https://www.youtube.com/watch?v=KN_XsZ9GDjQ';" />
          </picture>
          <p class="container__p">Une envolée de mots posée sur un groove de base Hip Hop. Les textes sentent le bon vin et s'appuient sur des sonorités swing ou funk permettant le déhanchement et la danse !</p>
      </div>
      
      <div class="container__div">
          <h3 class="container__h3">Crucial Rob - Sound System<br>(REGGAE / DUB)</h3>
          <picture class="container__picture">
              <img class="container__picture__img" src="../assets/crucial_rob.jpg" alt="Groupe Crucial Rob">
              <img class="container__picture__youtube" src="../assets/social/youtube.png" onclick="location.href='https://www.youtube.com/watch?v=hUpRt-x4oe8';" />
          </picture>
          <p class="container__p">Nourrit d’univers musicaux et de cultures du monde entier, il est envieux de pouvoir concocter ses propres sonorités, il créé alors le Prophecy Studio. <br>

C’est avec autant d’instruments organiques que de machines et synthétiseurs que Rob créé son univers musical et compose une musique cathartique puissante parfois hypnotique à la rythmique tribale et soutenue. </p>
      </div>
      <div class="container__div">
          <h3 class="container__h3">High Steppa - Sound System<br>(REGGAE / DUB)</h3>
          <picture class="container__picture">
              <img class="container__picture__img" src="../assets/High_new.jpg" alt="Groupe High Rockers">
          </picture>
          <p class="container__p">High steppa, en 2013 il commence à acheter, collectionner ses premiers vinyles reggae/roots/dub et ce fait inviter pour ses premières dances à Genève. En 2014 il rencontre Mighty Rockers sound systems avec qui ils fusionnent pour créer le High Rockers sound system et vont évoluer ensemble jusqu’en 2017. Aujourd’hui High Steppa se produit seul avec une énergie positive hors du commun. En passant du roots au dub avant-gardiste il vous fera skanker sec! stay tuned!</p>
      </div>
      <div class="container__div">
          <h3 class="container__h3">A.B.S. - Sound System<br>(REGGAE / DUB)</h3>
          <picture class="container__picture">
              <img class="container__picture__img" src="../assets/ABS_SoundSystem.jpg" alt="Groupe A.B.S">
          </picture>
          <p class="container__p">Anciennement un crew de graffiti né en 2004, ABS Sound System ce sont 5 amis tous originaires de Billom à coter de Clermont Ferrand. Réunis depuis 2017 avec déjà un demi stack en sono, nous proposons une danse allant du Root au Dub.</p>
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

    &__presentation{
        color: white;
        padding: 20px 10vw 0px 10vw ; // top right bottom left

        font-family:'Berlin'; font-size: 1em;
        font-weight: 400; color: white;
    }

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
        position: relative;

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
        &__youtube{
            position: absolute;
            top: 70px; left: 0; right: 0;
            width: 50px; height: 50px;

            @include media-device-max(900px){
                top: 25px; left: 0; right: 0; 
                width: 20px; height: 20px;
            }

            &:hover{
                cursor: pointer;
            }
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
