<template>
  <header class="header">
    <div class="container">
      <img class="header__img" src="../assets/img/dc-logo.png" alt="DC logo" />
      <ul class="header__list">
        <li v-for="(item, index) in menu" :key="index">
          <h1>{{ item.text }}</h1>
        </li>
      </ul>
    </div>
  </header>
</template>

<script>
export default {
  name: "AppHeader",
  data: function () {
    return {
      menu: [
        {
          text: "Character",
        },
        {
          text: "Comics",
        },
        {
          text: "Movies",
        },
        {
          text: "TV",
        },
        {
          text: "Games",
        },
        {
          text: "Collectibles",
        },
        {
          text: "Videos",
        },
        {
          text: "Fans",
        },
        {
          text: "News",
        },
        {
          text: "Shop",
        },
      ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
.header {
  width: 100%;
  height: 150px;
  background-color: white;

  &__img {
    height: 75%;
    display: flex;
    align-self: center;
  }

  &__list {
    display: flex;
    align-items: center;
    list-style: none;
    li {
      font-weight: 500;
      margin-right: 15px;

      h1 {
        font-size: 16px;
        line-height: 100px;
      }
    }
    #selected {
      color: #0282f9;
      border-bottom: 3px solid #0282f9;
    }
  }
}
</style>
