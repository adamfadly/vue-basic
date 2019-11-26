<template>
  <div id="blogs">
    <h2>{{ blogTitle }}</h2>
    <button @click="changeTitle">change title</button>
  </div>
</template>

<script>
export default {
  name: 'blogs',
  data() {
    return {
      blogTitle: 'this is so coolllll....'
    }
  },
  methods: {
    changeTitle() {
      this.blogTitle= 'Ganti Judul'
    }
  },
  created() {
    alert('this is hook of create')
  },
  beforeCreate() {
    alert('this is create hooks')
  },
  beforeUpdate() {
    alert('this is update')
  }
}
</script>

<style scoped>

</style>
