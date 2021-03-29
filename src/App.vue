<template>
  <form>
    <input type="checkbox" v-model="toggle" />
  </form>
  <HelloI18n v-if="toggle" />
  <template v-else>
    <NoneI18n />
    <OtherI18n />
  </template>
</template>

<script>
import HelloI18n from './components/HelloI18n.vue'
import NoneI18n from './components/NoneI18n.vue'
import OtherI18n from './components/OtherI18n.vue'

export default {
  name: 'App',
  components: {
    HelloI18n,
    NoneI18n,
    OtherI18n
  },
  data() {
    return {
      toggle: true
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
