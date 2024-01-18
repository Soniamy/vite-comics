<script>
export default {
  data() {
    return {
      navItems: [
        {
          text: 'Digital Comics',
          src: `comics-digital-comics.png`,
        },

        {
          text: 'DC Merchandise',
          src: `comics-merchandise.png`,
        },

        {
          text: 'Subscriptions',
          src: `comics-subscriptions.png`,
        },

        {
          text: 'Comic Shop Locator',
          src: `comics-shop-locator.png`,
        },

        {
          text: 'DC Power Visa',
          src: `dc-power-visa.svg`,
        },
      ],
    };
  },
  methods: {
    getImgPath(imgPath) {
      return new URL('../../public/buy-' + imgPath, import.meta.url).href;
    },
  },
};
</script>

<template>
  <nav class="container">
    <ul class="d-flex justify-around align-center">
      <li v-for="(navItem, index) in navItems" :key="index">
        <a href="#" class="d-flex align-center text-uppercase">
          <img :src="getImgPath(navItem.src)" :alt="navItem.text" />
          <span>{{ navItem.text }}</span>
        </a>
      </li>
    </ul>
  </nav>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/variables.scss' as *;
nav {
  background-color: $complementary--color;

  ul {
    padding: 1.2rem 0;

    img {
      width: 37px;
      margin-right: 1rem;
    }

    li {
      &:hover img {
        filter: brightness(2);
      }

      a {
        font-size: 0.7rem;
        color: $primary--color;
        margin-left: 35px;
      }
    }
  }
}
</style>
