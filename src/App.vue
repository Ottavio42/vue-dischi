<template>
  <div id="app">
    <Header />
    <main>
      <Dischi> </Dischi>
    </main>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Dischi from "./components/Dischi.vue";
export default {
  name: "App",
  components: {
    Header,
    Dischi,
  },
};
</script>

<style lang="scss">
@import "./assets/style/common.scss";
</style>