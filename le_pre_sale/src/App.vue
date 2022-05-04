<template>
  <HelloWorld/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  created() {
    document.title = 'Festival - Prés Salés';
  },
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Monoton&family=Share&display=swap');

*, *:before, *:after {
  box-sizing: border-box;
  margin: 0px 0px 0px 0px ; // top right bottom left
}
</style>
