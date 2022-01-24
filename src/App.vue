<template>
  <div
    id="app"
  >
    <Header
      :links="headerlinks"
    />
    <Main
      :maj-infos="majorInfos"
    />
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
          name: 'Home',
          href: '#',
        },
        {
          name: 'About',
          href: '#',
        },
        {
          name: 'Departments',
          href: '#',
        },
        {
          name: 'Articles',
          href: '#',
        },
      ],
      majorInfos: [
        {
          // eslint-disable-next-line quotes
          icon: `icon-1.png`,
          title: 'Same day appointments',
          text: 'Sed ut pespiciatis unde omnis iste natus error sit voluptatem accusantium',
        },
        {
          icon: 'icon-2.png',
          title: 'World class facilities',
          text: 'Sed ut pespiciatis unde omnis iste natus error sit voluptatem accusantium',
        },
        {
          icon: 'icon-3.png',
          title: 'Expert doctors',
          text: 'Sed ut pespiciatis unde omnis iste natus error sit voluptatem accusantium',
        },
        {
          icon: 'icon-4.png',
          title: 'Complementary therapies',
          text: 'Sed ut pespiciatis unde omnis iste natus error sit voluptatem accusantium',
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
