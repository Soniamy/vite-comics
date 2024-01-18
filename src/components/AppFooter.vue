<script>
export default {
  data() {
    return {
      navSections: [
        {
          title: 'Dc Comics',
          navItems: [
            'Characters',
            'Comics',
            'Movies',
            'TV',
            'Games',
            'Videos',
            'News',
          ],
        },

        {
          title: 'Shop',
          navItems: ['Shop DC', 'Shop DC Collectibles'],
        },

        {
          title: 'DC',
          navItems: [
            'Terms of Use',
            'Privacy policy(new)',
            'Ad Choices',
            'Advertising',
            'Jobs',
            'Subscriptions',
            'Talent Workshops',
            'CPSC Certificates',
            'Ratings',
            'Shop Help',
            'Contact Us',
          ],
        },

        {
          title: 'Sites',
          navItems: [
            'DC',
            'MAD Magazines',
            'DC Kids',
            'DC Universe',
            'DC Power Visa',
          ],
        },
      ],
    };
  },
  methods: {},
};
</script>

<template>
  <section id="navbar-container" class="container d-flex">
    <nav class="d-flex wrap column">
      <div
        class="nav-item"
        v-for="(navSection, index) in navSections"
        :key="index"
      >
        <span class="text-uppercase title">{{ navSection.title }}</span>
        <ul>
          <li v-for="(navItem, index) in navSection.navItems" :key="index">
            <a href="#" :alt="navItem">{{ navItem }}</a>
          </li>
        </ul>
      </div>
    </nav>

    <div class="img-container"></div>
  </section>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/variables.scss' as *;

#navbar-container {
  background-image: url('public/footer-bg.jpg');
  background-repeat: no-repeat;
  background-size: cover;
  height: 23rem;

  > * {
    width: 50%;
  }

  &.container {
    padding-top: 0;
    padding-bottom: 0;
  }

  .img-container {
    background-image: url('public/dc-logo.png');
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
    padding: 0;
  }

  nav {
    padding: 1.5rem 0;

    .nav-item {
      margin: 1rem 0;

      .title {
        font-weight: bold;
      }

      li {
        font-size: 0.7rem;
        padding-bottom: 0.2rem;

        &:first-of-type {
          padding-top: 0.7rem;
        }

        a {
          color: $icon--bg-color;

          &:hover {
            color: $primary--color;
          }
        }
      }
    }
  }
}
</style>
