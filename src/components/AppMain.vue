<template>
  <main>
    <div class="jumbotron"></div>
    <div class="series">
      <div class="current-series">
        <h3>current series</h3>
      </div>
      <div class="container">
        <div class="card-image" v-for="(item, index) in allCards" :key="index">
          <div class="img-thumb">
            <img :src="item.thumb" alt="" />
          </div>
          <p>
            {{ item.series }}
          </p>
        </div>
        <div class="load-btn">
          <button class="load-btn">load more</button>
        </div>
      </div>
    </div>
  </main>
</template>

<script>
export default {
  name: "AppMain",
  props: {
    allCards: Array,
  },
};
</script>

<style>
.jumbotron {
  height: 320px;
  background-image: url(../assets/img/jumbotron.jpg);
  background-size: cover;
}

.series {
  background-color: #303030;
}

.current-series {
  width: 200px;
  padding: 10px 25px;
  margin: 0 auto;
  background-color: #0282f9;
}

.current-series h3 {
  color: white;
  text-transform: uppercase;
}

.card-image {
  width: calc(100% / 6);
}

.card-image p {
  font-size: 12px;
  text-align: center;
  text-transform: uppercase;
  color: white;
}

.img-thumb {
  margin: 1rem;
}

.img-thumb img {
  width: 150px;
  height: 150px;
  padding: 10px;
}

.load-btn {
  margin: 1rem auto;
}

.load-btn button {
  width: 180px;
  text-transform: uppercase;
  padding: 10px 20px;
  border: 0px;
  margin: 1rem;
  color: white;
  background-color: #0282f9;
  font-weight: 700;
}
</style>
