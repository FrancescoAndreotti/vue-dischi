<template>
  <div id="app">
    <Header />
    <CardContainer />
  </div>
</template>

<script>
import CardContainer from "./components/CardContainer.vue";
import Header from "./components/Header.vue";
export default {
  name: "App",
  components: {
    CardContainer,
    Header,
  },
};
</script>

<style lang="scss">
@import "@/scss/app";
</style>
