<template>
  <div>
    <AlbumsPageVue />
    <div class="content">
      <div
        v-for="element in arrAlbums"
        :key="element"
        class="box-content"
        :img-url="element.poster"
        :title="element.title"
        :author="element.author"
        :year="element.year"
      /> {{ element.imgUrl }}
    </div>
  </div>
</template>

<script>
import axios from 'axios';
import AlbumsPageVue from './AlbumsPage.vue';

export default {
  name: 'MainPage',
  components: {
    AlbumsPageVue,
  },
  data() {
    return {
      arrAlbums: null,
      urlAPI: 'https://flynn.boolean.careers/exercises/api/array/music',
    };
  },
  created() {
    axios.get(this.urlAPI)
      .then((axiosResponse) => {
        console.log(axiosResponse);
        this.arrAlbums = axiosResponse.data.response;
      });
  },
};
</script>

<style lang="scss" scoped>

.content {
  height: calc(100vh - 77px);
  max-width: 900px;
  margin: auto;
  display: flex;
  justify-content: center;
  align-items: center;
  border: 2px solid yellow;
}

.box-content {
  height: 50px;
  width: 50px;
  border: 1px solid red;
}
</style>
