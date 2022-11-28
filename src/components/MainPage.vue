<template>
  <div class="container">
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

.content {
  height: calc(100vh - 56px);
  display: flex;
  justify-content: center;
  align-items: center;
}

.content-box {
  max-width: 1000px;
  border: 2px solid yellow;
}
</style>
