<template>
  <div class="container">
    <h1>
      Spotify
    </h1>
    <div class="content">
      <div class="content-box">
        <AlbumsPageVue />
      </div>
    </div>
  </div>
</template>

<script>
import AlbumsPageVue from './AlbumsPage.vue';

export default {
  name: 'MainPage',
  components: {
    AlbumsPageVue,
  },
};
</script>

<style lang="scss" scoped>
h1 {
  text-align: center;
  color: rgb(194, 194, 194);
  background-color: rgb(49, 49, 49);
  padding: .6rem 0;
}
</style>
