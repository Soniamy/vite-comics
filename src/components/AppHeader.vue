<script>
export default {
  name: 'AppHeader',

  data() {
    return {
      activeIndex: 1,
      navItems: [
        {
          text: 'Characters',
          url: '#',
          active: false,
        },

        {
          text: 'Comics',
          url: '#',
          active: true,
        },

        {
          text: 'Movies',
          url: '#',
          active: false,
        },

        {
          text: 'TV',
          url: '#',
          active: false,
        },

        {
          text: 'Games',
          url: '#',
          active: false,
        },

        {
          text: 'Collectibles',
          url: '#',
          active: false,
        },

        {
          text: 'Videos',
          url: '#',
          active: false,
        },

        {
          text: 'Fans',
          url: '#',
          active: false,
        },

        {
          text: 'News',
          url: '#',
          active: false,
        },

        {
          text: 'Shop',
          url: '#',
          active: false,
        },
      ],
    };
  },
  methods: {},
};
</script>

<template>
  <header>
    <div class="container">
      <nav class="d-flex justify-between align-center">
        <a class="logo-container" href="#">
          <img src="/public/dc-logo.png" alt="logo" title="logo" />
        </a>

        <ul class="d-flex">
          <li
            class="text-uppercase d-flex"
            @click="activeIndex = index"
            v-for="(navItem, index) in navItems"
            :key="index"
            :class="{ ' active': index == activeIndex }"
          >
            <a :href="navItem.url" :alt="navItem.text">{{ navItem.text }}</a>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/variables.scss' as *;
header {
  background-color: $primary--color;

  .container {
    padding-top: 0;
    padding-bottom: 0;
  }

  nav {
    height: 100px;

    .logo-container {
      width: 60px;
    }

    ul {
      height: 100%;

      li {
        margin-right: 2.3rem;
        line-height: 100px;

        &.active {
          border-bottom: 3px solid $complementary--color;
          cursor: pointer;

          a {
            color: $complementary--color;
          }
        }

        a {
          font-size: 0.7rem;
          font-weight: bold;
          color: $darker--icon--bg-color;
        }
      }
    }
  }
}
</style>
