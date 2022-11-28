<template>
  <div>
    <HeaderPageVue />
    <MainPageVue />
  </div>
</template>

<script>
import MainPageVue from './components/MainPage.vue';
import HeaderPageVue from './components/HeaderPage.vue';

export default {
  components: {
    MainPageVue,
    HeaderPageVue,
  },
};
</script>

<style lang="scss">
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    background-color: rgb(35, 35, 35);
    color: rgb(225, 225, 225);
    text-align: center;
}
</style>
