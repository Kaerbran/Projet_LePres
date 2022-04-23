<template>
  <div>
    <NavSite />

    <div>
      ici la page d'acceuil
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
