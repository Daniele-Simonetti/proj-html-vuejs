<template>
  <main>
    <!-- creo il jumbo con lo sfondo che copre anche l'header -->
    <div class="jumbo">
      <div class="row">
        <div class=" jumbo-text">
          <h1>Caring <span>For Life</span></h1>
          <p>
            Kind words can be short and easy to speak, but their echoes are truly endless.
            Avada Health focuses on you as if it was our own family.
          </p>
          <button
            type="button"
            class="btn btn-primary btn-lg text-uppercase"
          >
            Learn More
          </button>
        </div>
      </div>
    </div>

    <!-- creo la prima / 5 sezione del main -->
    <div class="welcome">
      <div class="row">
        <div class="col-6 offset-3 text-center general-text">
          <h2>Welcome to Avada Health</h2>
          <p>
            Sed ut pespiciatis unde omnis iste natus error sit
            voluptatem accusantium doloremque laudantium,
            totam rem aperiam, eaque ipsa quae ab illo
          </p>
        </div>
      </div>
    </div>
    <div class=" box-cards">
      <div class="row cards justify-content-between">
        <div
          v-for="(info, index) in majInfos"
          :key="index"
          class=""
        >
          <img
            :src="require(`../assets/images/${info.icon}`)"
            :alt="info.title"
          >
          <h3>{{ info.title }}</h3>
          <p>{{ info.text }}</p>
        </div>
      </div>
    </div>
  </main>
</template>

<script>
export default {
  name: 'Main',
  props: {
    majInfos: {
      type: Array,
      default() {
        return [];
      },
    },
  },
};
</script>

<style lang="scss" scoped>
.jumbo {
  background-image: url('../assets/images/header-image-homepage.jpg');
  background-repeat: no-repeat;
  background-size: cover;

  // height: 865px;
  .jumbo-text {
    width: 51%;
    margin: 15% auto;
    h1 {
      color: white;
    }
    p {
      color: white;
      font-size: 1.1em;
    }
    button {
      font-size: 0.9em;
      background-color: #39afbb;
      border: 0;
      border-radius: 0.2rem;
      padding: 0.5em 1.8em;
      margin-top: 0.5em;
      &:active,
      &:focus {
        border: 0;
        box-shadow: 0 0 0 0;
      }
    }
  }
}
.general-text {
  font-weight: 100;
  padding: 0 7em;
  margin-top: 4em;
  h2 {
    font-weight: 100;
    margin-bottom: 0.5em;
  }
  p {
    font-weight: 500;
    line-height: 2em;
  }
}
.box-cards {
  width: 70%;
  margin: 5em auto;
  .cards {
    div {

      flex-basis: calc((100% / 4) - 2em);
      text-align: center;
    }
  }

}
</style>
