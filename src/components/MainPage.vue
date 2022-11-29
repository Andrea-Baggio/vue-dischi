<template>
  <div>
    <div class="content">
      <div
        v-for="element in arrAlbums"
        :key="element"
        class="box-content"
      >
        <div class="poster">
          <img
            :src="element.poster"
            alt="poster"
          >
        </div>

        <h3>{{ element.title }}</h3>
        <div class="author">
          {{ element.author }}
        </div>
        <div class="year">
          {{ element.year }}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  name: 'MainPage',
  components: {

  },
  data() {
    return {
      arrAlbums: null,
      urlApi: 'https://flynn.boolean.careers/exercises/api/array/music',
    };
  },
  created() {
    axios.get(this.urlApi)
      .then((axiosResponse) => {
        console.log(axiosResponse);
        this.arrAlbums = axiosResponse.data.response;
      });
  },
};
</script>

<style lang="scss" scoped>

.content {
  height: calc(100vh - 57px);
  max-width: 1000px;
  margin: auto;
  display: flex;
  flex-direction: column;
  justify-content: center;
  flex-wrap: wrap;
  gap: 1rem;
  padding: 3rem 0;
  font-size: .8em;
}

.box-content {
  display: flex;
  flex-direction: column;
  flex-basis: calc((100% - 1rem) / 5);
}

.poster {
  max-width: 130px;
  img {
    width: 100%;
  }
}
</style>
