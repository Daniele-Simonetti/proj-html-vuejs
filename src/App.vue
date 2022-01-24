<template>
  <div
    id="app"
  >
    <Header
      :links="headerlinks"
    />
    <Main />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Main from './components/Main.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer,
  },
  data() {
    return {
      headerlinks: [
        {
          name: 1,
          href: '#',
        },
        {
          name: 1,
          href: '#',
        },
        {
          name: 1,
          href: '#',
        },
        {
          name: 1,
          href: '#',
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "~bootstrap/scss/bootstrap";
@import './assets/scss/_variables.scss';
#app {
  font-family: $fontFamily;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
