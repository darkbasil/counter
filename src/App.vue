<template>
  <div id="app">
    <num-setter></num-setter>
    <num-getter></num-getter>
  </div>
</template>

<script>
import NumSetter from './components/NumSetter.vue'
import NumGetter from './components/NumGetter.vue'

export default {
  name: 'app',
  components: {
    NumSetter,
    NumGetter
  }
}
</script>

<style scoped>

</style>
