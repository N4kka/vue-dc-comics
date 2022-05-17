<template>
  <header class="header">
    <div class="header__container">
      <img class="header__img" src="../assets/img/dc-logo.png" alt="DC logo" />
      <ul class="header__list">
        <li>Character</li>
        <li id="selected">Comics</li>
        <li>Movies</li>
        <li>TV</li>
        <li>Games</li>
        <li>Collectibles</li>
        <li>Videos</li>
        <li>Fans</li>
        <li>News</li>
        <li>Shop</li>
      </ul>
    </div>
  </header>
</template>

<script>
export default {
  name: "AppHeader",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
.header {
  width: 100%;
  height: 100px;
  margin-top: 2rem;
  background-color: white;

  &__container {
    width: 60%;
    height: 100%;
    line-height: 100px;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
  }

  &__img {
    height: 75%;
    display: flex;
    align-self: center;
  }

  &__list {
    display: flex;
    list-style: none;
    li {
      font-weight: 500;
      margin-right: 15px;
    }
    #selected {
      color: #0282f9;
      border-bottom: 3px solid #0282f9;
    }
  }
}
</style>
