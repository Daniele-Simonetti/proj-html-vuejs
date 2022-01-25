<template>
  <div
    id="app"
  >
    <Header
      :links="headerlinks"
    />
    <Main
      :maj-infos="majorInfos"
      :doctors="docs"
      :services="healthservices"
      :fac-highlight="facilitiesMost"
      :lasticons="lastMainIcons"
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
      docs: [
        {
          img: 'doctor-1-200x206.jpg',
          name: 'Jon Snow',
          job: 'Anesthesiologist',
          description: 'At vero eos et accusamus et iusto odio dignissimo ducimus qui blanditis praesentium voluptatum deleniti atque',
          icons: [
            {
              facebook: 'FB',
            },
            {
              twitter: 'TW',
            },
            {
              instagram: 'IN',
            },
          ],
        },
        {
          img: 'doctor-2-200x206.jpg',
          name: 'Tony Stark',
          job: 'Cardiologist',
          description: 'At vero eos et accusamus et iusto odio dignissimo ducimus qui blanditis praesentium voluptatum deleniti atque',
          icons: [
            {
              facebook: 'FB',
            },
            {
              twitter: 'TW',
            },
            {
              instagram: 'IN',
            },
          ],
        },
        {
          img: 'doctor-3-200x206.jpg',
          name: 'Anna Smith',
          job: 'Nurse Practitioner',
          description: 'At vero eos et accusamus et iusto odio dignissimo ducimus qui blanditis praesentium voluptatum deleniti atque',
          icons: [
            {
              facebook: 'FB',
            },
            {
              twitter: 'TW',
            },
            {
              instagram: 'IN',
            },
          ],
        },
      ],
      healthservices: [
        {
          icon: 'icon-14.png',
          title: 'Rehabilitation center',
          explanation: 'At vero eos et accusamus et iusto odio didnissimos ducimus qui blanditis praesentium voluptatum deleniti atque corrupti quos dolores et quas',
        },
        {
          icon: 'icon-15.png',
          title: 'Dental implants',
          explanation: 'At vero eos et accusamus et iusto odio didnissimos ducimus qui blanditis praesentium voluptatum deleniti atque corrupti quos dolores et quas',
        },
        {
          icon: 'icon-16.png',
          title: 'Medicine research',
          explanation: 'At vero eos et accusamus et iusto odio didnissimos ducimus qui blanditis praesentium voluptatum deleniti atque corrupti quos dolores et quas',
        },
        {
          icon: 'icon-11.png',
          title: 'Blood bank',
          explanation: 'At vero eos et accusamus et iusto odio didnissimos ducimus qui blanditis praesentium voluptatum deleniti atque corrupti quos dolores et quas',
        },
        {
          icon: 'icon-12.png',
          title: 'Pharmaceutical advice',
          explanation: 'At vero eos et accusamus et iusto odio didnissimos ducimus qui blanditis praesentium voluptatum deleniti atque corrupti quos dolores et quas',
        },
        {
          icon: 'icon-13.png',
          title: 'Medical consuealing',
          explanation: 'At vero eos et accusamus et iusto odio didnissimos ducimus qui blanditis praesentium voluptatum deleniti atque corrupti quos dolores et quas',
        },
      ],
      facilitiesMost: [
        {
          title: 'Emergency Care',
          exp: 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium dolerumque laudantium, totam rem aperiam, eaque',
        },
        {
          title: 'Expert Diagnostic',
          exp: 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium dolerumque laudantium, totam rem aperiam, eaque',
        },
        {
          title: 'Superb Rehabilitation',
          exp: 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium dolerumque laudantium, totam rem aperiam, eaque',
        },
      ],
      lastMainIcons: [
        {
          icon: 'client-logos-3.png',
          alt: 'client-logos-3.png',
        },
        {
          icon: 'client-logos-1.png',
          alt: 'client-logos-1.png',
        },
        {
          icon: 'client-logos-4.png',
          alt: 'client-logos-4.png',
        },
        {
          icon: 'client-logos-2.png',
          alt: 'client-logos-2.png',
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
