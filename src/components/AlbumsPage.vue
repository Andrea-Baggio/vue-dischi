<template>
  <div class="container">
    <img
      :src="imgUrl"
      alt="image"
    >
    <!-- <h4>{{ title }}</h4>
      <div>{{ author }}</div>
      <div>{{ year }}</div> -->
  </div>
</template>

<script>
export default {
  name: 'AlbumsPage',
  props: {
    imgUrl: String,
    // title: String,
    // author: String,
    // year: String,
  },
};
</script>

<style>

</style>
