<template>
  <div class="body">
    <HeaderPageVue />
    <MainPageVue />
  </div>
</template>

<script>
import HeaderPageVue from './components/HeaderPage.vue';
import MainPageVue from './components/MainPage.vue';

// https://flynn.boolean.careers/exercises/api/array/music

export default {
  components: {
    HeaderPageVue,
    MainPageVue,
  },
};
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Lato:wght@100;300;400;700;900&display=swap');

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

.body {
    background-color: rgb(35, 35, 35);
    color: rgb(225, 225, 225);
    text-align: center;
    font-family: 'Lato', sans-serif;
}
</style>
