<script>
import HelloWorld from './components/HelloWorld.vue'
import Header from './components/Header.vue';
import Main from './components/Main.vue';
import 'bootstrap/dist/css/bootstrap.css'

export default {
  components: {
    Header,
    Main,

  },
  data() {
    return {

    }
  },
  methods: {
    testBody() {
      console.log('ok bady')
    },

    }
  }

</script>

<template>
  <Header  />
  <Main />
</template>

<style></style>
