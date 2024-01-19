<script>
export default {
  name: 'SingleCard',
  props: {
    thumb: String,
    price: String,
    series: String,
    type: String,
  },
};
</script>

<template>
  <article class="card">
    <a href="#">
      <div class="img-container">
        <img :src="thumb" :alt="series" :title="series + '\nPrice:' + price" />
      </div>
      <span class="text-uppercase title-comic d-flex justify-between">{{
        series
      }}</span>
    </a>
  </article>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/variables.scss' as *;
.card {
  width: calc(100% / 6 - 2rem);
  margin: 1rem;
  a {
    color: $primary--color;
  }
  .img-container {
    width: 120px;
    height: 120px;
    overflow: hidden;
    border-radius: 20px;
    border: 1px solid white;
  }
  .text-uppercase {
    margin-top: 5px;
  }
  .title-comic {
    line-height: 20px;
    &.title-comic {
      justify-content: center;
      text-align: center;
    }
  }
  &:hover img {
    filter: contrast(1.5);
  }
}
</style>
