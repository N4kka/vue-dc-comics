<template>
  <footer>
    <div class="footer-top">
      <div class="container">
        <div class="footer-left">
          <ul class="footer-list">
            <li v-for="(item, index) in footerMenu" :key="index">
              <h4>{{ item.title }}</h4>
              <p>{{ item.text }}</p>
            </li>
          </ul>
          <ul class="footer-list">
            <li v-for="(element, index) in secondList" :key="index">
              <h4>{{ element.title }}</h4>
              <p>{{ element.text }}</p>
            </li>
          </ul>
          <ul class="footer-list">
            <li v-for="(list, index) in thirdList" :key="index">
              <h4>{{ list.title }}</h4>
              <p>{{ list.text }}</p>
            </li>
          </ul>
          <ul class="footer-list">
            <li v-for="(shop, index) in fourthList" :key="index">
              <h4>{{ shop.title }}</h4>
              <p>{{ shop.text }}</p>
            </li>
          </ul>
        </div>
        <div class="footer-right"></div>
      </div>
    </div>
    <div class="footer-bottom">
      <div class="container">
        <div class="shop">
          <button>SIGN-UP NOW!</button>
        </div>
        <div class="social">
          <h2>follow us</h2>
          <ul class="social-icons">
            <li v-for="(images, index) in socials" :key="index">
              <img :src="require(`../assets/img/${images.img}`)" alt="" />
            </li>
          </ul>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "AppFooter",
  data: function () {
    return {
      footerMenu: [
        {
          title: "dc comics",
          text: "Characters",
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
          text: "Videos",
        },
        {
          text: "News",
        },
      ],
      secondList: [
        {
          title: "dc",
          text: "Terms Of Use",
        },
        {
          text: "Privacy policy (New)",
        },
        {
          text: "Ad Choices",
        },
        {
          text: "Advertising",
        },
        {
          text: "Jobs",
        },
        {
          text: "Subscriptions",
        },
        {
          text: "Talent Workshops",
        },
        {
          text: "CPSC Certificates",
        },
        {
          text: "Ratings",
        },
        {
          text: "Shop Help",
        },
        {
          text: "Contact Us",
        },
      ],
      thirdList: [
        {
          title: "sites",
          text: "DC",
        },
        {
          text: "MAD Magazine",
        },
        {
          text: "DC Kids",
        },
        {
          text: "DC Universe",
        },
        {
          text: "DC Power Visa",
        },
      ],
      fourthList: [
        {
          title: "shop",
          text: "Shop DC",
        },
        {
          text: "Shop DC Collectibles",
        },
      ],
      socials: [
        {
          img: "footer-facebook.png",
        },
        {
          img: "footer-twitter.png",
        },
        {
          img: "footer-youtube.png",
        },
        {
          img: "footer-pinterest.png",
        },
        {
          img: "footer-periscope.png",
        },
      ],
    };
  },
};
</script>

<style>
footer {
  width: 100%;
  height: 500px;
}

.footer-top {
  height: 380px;
  display: flex;
  background-image: url(../assets/img/footer-bg.jpg);
  background-repeat: no-repeat;
  background-size: cover;
}

.footer-left {
  width: 50%;
  height: 100%;
  display: flex;
  flex-wrap: wrap;
}

.footer-list {
  width: calc(100% / 3);
  margin-top: 0.5rem;
  color: white;
  list-style: none;
}

.footer-list h4 {
  text-transform: uppercase;
  padding-bottom: 10px;
}

.footer-list p {
  color: gray;
  font-size: 12px;
}

.footer-right {
  width: 50%;
  height: 100%;
  background-image: url(../assets/img/dc-logo-bg.png);
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
}

.footer-bottom {
  height: 120px;
  background-color: #303030;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.shop {
  display: flex;
  align-items: center;
}

.shop button {
  color: white;
  padding: 15px;
  border-color: #0282f9;
  font-weight: 700;
  background-color: #303030;
}

.social {
  display: flex;
  align-items: center;
}

.social h2 {
  text-transform: uppercase;
  color: #0282f9;
}

.social-icons {
  display: flex;
  list-style: none;
}

.social-icons li {
  padding: 0 10px;
}
</style>
