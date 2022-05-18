<template>
  <div id="app">
    <!-- HEADER -->
    <AppHeader />
    <!-- /HEADER -->

    <!-- MAIN -->
    <div class="background">
      <div class="main-text">&rarr; Content goes here &larr;</div>
    </div>
    <!-- /MAIN -->

    <!-- PREFOOTER -->
    <AppPreFooter />
    <!-- /PREFOOTER -->

    <!-- FOOTER -->
    <AppFooter />
    <!-- /FOOTER -->
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";
import AppPreFooter from "./components/AppPreFooter.vue";
import AppFooter from "./components/AppFooter.vue";

export default {
  name: "App",
  components: {
    AppHeader,
    AppPreFooter,
    AppFooter,
  },
};
</script>

<style lang="scss">
@import "./style/common.scss";

// COMMON
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  font-family: "Roboto", sans-serif;
}

body {
  background-color: black;
}

.container {
  width: 60%;
  height: 100%;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
}

// MAIN
.background {
  height: 100px;
  background-color: #1c1c1c;
  color: white;
}

.main-text {
  width: 60%;
  height: 100%;
  line-height: 100px;
  margin: 0 auto;
  font-size: 2rem;
  font-weight: 500;
}
</style>
