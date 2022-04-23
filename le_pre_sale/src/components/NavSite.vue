<template>
  <div class="bandeau">
    <p class="bandeau__date">24 Juin à partir de 18h</p>
    <div class="bandeau__achat">
        <button class="bandeau__achat__btt">Billeterie</button>
        <img class="bandeau__achat__img" src="" alt="">    
    </div>    
  </div>
</template>

<script>
export default {
  name: 'NavSite'
}
</script>

<style scoped lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Monoton&family=Share&display=swap');

*, *:before, *:after {
  box-sizing: border-box;
  margin: 0px 0px 0px 0px ; // top right bottom left
}

.bandeau{
    display: flex;
    justify-content: center;

    background-color: rgba(217, 229, 192, 1);
    padding: 20px 20px 20px 20px ; // top right bottom left

    &__date{
        display: inline-block;
        margin: auto 0px auto auto ; // top right bottom left

        font-family:'Monoton',sans-serif;
        color: rgba(204, 96, 63, 1);
    }
    &__achat{
        margin-left: auto;

    }
    &__achat__btt {
        display:inline-block;
        padding:0.7em 1.4em;
        margin:0 0.3em 0.3em 0;
        border-radius:0.15em;
        box-sizing: border-box;
        text-decoration:none;
        font-family:'Monoton',sans-serif;
        text-transform:uppercase;
        font-weight:400;
        color:#FFFFFF;
        background-color:rgba(204, 96, 63, 1);
        box-shadow:inset 0 -0.6em 0 -0.35em rgba(0,0,0,0.17);
        text-align:center;
        position:relative;
    }
    &__achat__img{

    }

//Tuto pour centrer correctement les élements:
//https://stackoverflow.com/questions/38948102/center-one-and-right-left-align-other-flexbox-element

}

</style>
