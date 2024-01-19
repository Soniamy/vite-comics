<script>
export default {
  data() {
    return {
      path: 'public/footer-',
      socialLinks: [
        {
          url: 'facebook',
          description: 'Facebook',
        },

        {
          url: 'twitter',
          description: 'Twitter',
        },

        {
          url: 'youtube',
          description: 'Youtube',
        },

        {
          url: 'pinterest',
          description: 'Pinterest',
        },

        {
          url: 'periscope',
          description: 'Google Maps',
        },
      ],
    };
  },

  methods: {
    getImgPath(imgPath) {
      return new URL('../../public/footer-' + imgPath + '.png', import.meta.url)
        .href;
    },
  },
};
</script>

<template>
  <section id="social-links" class="container d-flex justify-between">
    <a href="" class="btn text-uppercase d-flex align-center">Sign-Up Now!</a>
    <div class="social-links-container d-flex align-center">
      <span class="text-uppercase">Follow Us</span>
      <ul class="d-flex">
        <li v-for="(socialLink, index) in socialLinks" :key="index">
          <a href="#"
            ><img
              :src="getImgPath(socialLink.url)"
              :alt="socialLink.description + '\'s icon'"
              :title="socialLink.description + '\'s icon'"
          /></a>
        </li>
      </ul>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/variables.scss' as *;
#social-links {
  background-color: $lighter--primary--color;

  a {
    color: $primary--color;
  }

  ul li {
    margin-left: 1rem;

    a:hover {
      filter: brightness(2);
    }
  }

  span {
    font-weight: bold;
    color: $complementary--color;
  }

  .btn {
    padding: 0.7rem;
    border: 2px solid $complementary--color;
    font-size: 0.9rem;
  }
}
</style>
