<template>
    <Navigation/>

</template>

<script>
import Navigation from './components/Navigation.vue'

export default {
  name: 'HelloWorld',
  components: { 
      Navigation, 
    },
  props: {
    msg: String
  }
}
</script>

<style scoped lang="scss">

</style>
