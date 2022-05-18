<template>
  <main>
    <div class="jumbotron"></div>
    <div class="series">
      <div class="container">
        <div class="current-series">
          <h3>current series</h3>
        </div>
        <div class="card-image" v-for="(item, index) in cards" :key="index">
          <img :src="require(`../assets/img/${cards.thumb}`)" alt="" />
        </div>
      </div>
    </div>
  </main>
</template>

<script>
export default {
  name: "AppMain",
  props: {
    cards: Array,
  },
};
</script>

<style>
main {
  height: 700px;
}

.jumbotron {
  height: 320px;
  background-image: url(../assets/img/jumbotron.jpg);
  background-size: cover;
}

.series {
  height: 100%;
  position: relative;
  background-color: #303030;
}

.current-series {
  height: 50px;
  padding: 5px 15px;
  line-height: 40px;
  position: absolute;
  top: -30px;
  background-color: #0282f9;
}

.current-series h3 {
  color: white;
  text-transform: uppercase;
}

.card-img {
  width: calc(100% / 6);
  height: 50px;
}
</style>
