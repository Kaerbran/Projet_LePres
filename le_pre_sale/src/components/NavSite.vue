<template>
  <div class="bandeau">
    <p class="bandeau__date">24 Juin à partir de 18h</p>   
  </div>
</template>

<script>
export default {
  name: 'NavSite'
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

.bandeau{
    display: flex;
    justify-content: center;

    background-color: rgba(217, 229, 192, 1);
    padding: 20px 20px 20px 20px ; // top right bottom left

    &__date{
        display: inline-block;
        margin: auto ; 

        font-family:'Monoton',sans-serif; font-size: 1.5em;
        color: rgba(204, 96, 63, 1);
    }
}

</style>
