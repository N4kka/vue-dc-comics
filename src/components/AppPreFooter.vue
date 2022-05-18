<template>
  <section class="prefooter">
    <div class="container">
      <ul class="icons-list">
        <li v-for="(item, index) in icons" :key="index">
          <img :src="require(`../assets/img/${item.img}`)" alt="" />
          <h3>{{ item.text }}</h3>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppPreFooter",
  data: function () {
    return {
      icons: [
        {
          img: "buy-comics-digital-comics.png",
          text: "digital comics",
        },
        {
          img: "buy-comics-merchandise.png",
          text: "dc merchandise",
        },
        {
          img: "buy-comics-subscriptions.png",
          text: "subscription",
        },
        {
          img: "buy-comics-shop-locator.png",
          text: "comic shop locators",
        },
        {
          img: "buy-dc-power-visa.svg",
          text: "dc power visa",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.prefooter {
  height: 150px;
  background-color: #0282f9;
  padding: 2rem 0;

  .icons-list {
    display: flex;
    list-style: none;
    text-transform: uppercase;
    color: white;

    li {
      width: calc(100% / 5);
      display: flex;
      align-items: center;

      img {
        width: 20%;
        margin: 0 20px;
      }

      h3 {
        font-size: 9px;
      }
    }
  }
}
</style>
