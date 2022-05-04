<template>
  <div class="container">
      <h2 class="container__h2" >Le Lieu</h2>
      <div class="container_2" >
        <GoogleMap class="container__GoogleMap" :api-key="GoogleMapsKey" :center="center" :zoom="15">
          <Marker :options="{ position: center }" />
        </GoogleMap>
        <p class="container__p">
          <b>L'adresse :</b><br>
          Parc à daims - Festival Prés Salés<br>
          5B Avenue Nessel,<br>
          68750 Soultzmatt<br>
        </p>
      </div>
  </div>
</template>

<script>
import { defineComponent } from "vue";
import { GoogleMap, Marker } from "vue3-google-map";

export default defineComponent({
  components: { GoogleMap, Marker },
  setup() {
    const center = { lat: 47.968752, lng: 7.222412 };

    return { center };
  },
  data() {
    return {
      GoogleMapsKey : process.env.GOOGLEMAPS_KEY,
    }
  },
});

//Code pour acceder à des variables .env
//console.log(process.env.GOOGLEMAPS_KEY)
</script>

<style scoped lang="scss">
@mixin media-device-max($_max-device-width){
    @media screen and (max-device-width: $_max-device-width){
        &{ @content; }
    }
}

*, *:before, *:after {
  box-sizing: border-box;
  margin: 0px 0px 0px 0px ; // top right bottom left
}

.container_2{
  display: flex;
  flex-wrap: wrap;

  width: 100%;

  @include media-device-max(900px){
    flex-direction: column-reverse;
  }
}

.container{
  display: flex;
  flex-wrap: wrap;

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

  &__GoogleMap{
    width: 65%; height: 500px;

    @include media-device-max(900px){
    width: 100%;
  }
  }

  &__p{
    margin: 0px 0px 0px 15px ; // top right bottom left
    
    font-family:'Share',sans-serif; font-size: 1em;
    font-weight: 400;
  }
}

</style>
