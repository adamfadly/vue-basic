<template>
  <div id="add">
    <h1>address</h1>
    <div v-for="(alamat, index) in alamats" :key="index">
      <span>{{ alamat.name }} alamat {{ alamat.alamat }}</span>

    </div>
  </div>
</template>

<script>

export default {
  name: 'Address',
  props: ['alamats'],
  data() {
    return {

    }
  }
}
</script>
