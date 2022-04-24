<template>
  <div>
    <NavSite />

    <div>
      <picture>
        <img src="" alt="">
      </picture>
      <div>
        <div>
          <p>Le Pré Salé commence dans :</p>
          
        </div>
        <button>

        </button>
      </div>
    </div>

    <LaProgrammation />
    <LesAnimations />
    <LeLieux />
  </div>
</template>

<script>
import NavSite from "../components/NavSite"
import LaProgrammation from "../components/LaProgrammtion"
import LesAnimations from "../components/LesAnimations"
import LeLieux from "../components/LeLieux"

export default {
  name: 'HelloWorld',
  components: {
    NavSite,
    LaProgrammation,
    LesAnimations,
    LeLieux
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
*, *:before, *:after {
  box-sizing: border-box;
  margin: 0px 0px 0px 0px ; // top right bottom left
}

</style>
