<template>
  <div id="app">
    <h1>{{ title }}</h1>
    <Navbar />
  </div>
</template>

<script>
import Navbar from './Navbar'




export default {
  name: 'app',
  components: {
    Navbar,
  },

  data () {
    return {
     title: 'I will succes in software Development',
    }
  },
  methods: {

  }
}
</script>

<style>
#app{
  padding: 100px 200px;
}
h1 {
  color: #444;
  font-weight: normal;
  text-align: center;
}
</style>
