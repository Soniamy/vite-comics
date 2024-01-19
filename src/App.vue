<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import AppMainNavbar from './components/AppMainNavbar.vue';
import AppFooterLink from './components/AppFooterLink.vue';

export default {
  data() {
    return {};
  },
  components: {
    AppHeader,
    AppMain,
    AppMainNavbar,
    AppFooter,
    AppFooterLink,
  },
  methods: {},
};
</script>

<template>
  <AppHeader />

  <main>
    <AppMain />
    <AppMainNavbar />
  </main>
  <footer>
    <AppFooter />
    <AppFooterLink />
  </footer>
</template>

<style lang="scss">
@use 'assets/scss/partials/variables.scss' as *;
@use 'assets/scss/main' as *;
@import 'assets/scss/partials/reset';

body {
  color: $primary--color;
}
</style>
