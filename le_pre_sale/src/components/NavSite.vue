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
*, *:before, *:after {
  box-sizing: border-box;
  margin: 0px 0px 0px 0px ; // top right bottom left
}

.bandeau{
    display: flex;
    justify-content: center;

    background-color: rgba(217, 229, 192, 1);

    &__date{
        display: inline-block;
        margin-left: auto;
    }
    &__achat{
        margin-left: auto;

    }
    &__achat__btt {

    }
    &__achat__img{

    }

//Tuto pour centrer correctement les élements:
//https://stackoverflow.com/questions/38948102/center-one-and-right-left-align-other-flexbox-element

}

</style>
