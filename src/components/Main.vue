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
          <h3 class="text-uppercase">
            {{ info.title }}
          </h3>
          <p>{{ info.text }}</p>
        </div>
      </div>
    </div>
    <div class="ourDoc">
      <div class="row justify-content-center text-center text-box">
        <img
          :src="require(`../assets/images/icon-5.png`)"
          alt="doc-logo"
          class="doc-logo"
        >
        <h2 class="text-uppercase">
          Meet our Doctors
        </h2>
        <p>
          Sed ut perspiciatis unde omnis iste natus error sit voluptatem
          accusantium dolorumque laudantium,
          totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae
        </p>
      </div>
      <div class="row doc-box justify-content-between">
        <div
          v-for="(doc, i) in doctors"
          :key="i"
          class="doc-card"
        >
          <img
            :src="require(`../assets/images/${doc.img}`)"
            :alt="doc.name"
          >
          <div class="card-text">
            <h3 class="text-uppercase">
              {{ doc.name }}
            </h3>
            <h4>{{ doc.job }}</h4>
            <p>{{ doc.description }}</p>
            <div>
              <i>1</i>
              <i>2</i>
              <i>3</i>
            </div>
          </div>
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
    doctors: {
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
  margin: 1em auto;
  .cards {
    div {
      padding: 0;
      flex-basis: calc((100% / 4) - 2em);
      text-align: center;
      h3 {
        font-size: 0.9em;
      }
      p {
        text-align: justify;
        line-height: 2.3em;
        font-size: 0.8em;
        padding: 0 0.4em;
        word-spacing: 1px;
      }
      img {
        width: 30%;
      }
    }
  }
}
.ourDoc {
  .doc-logo {
    margin-top: 4em;
    width: 6%;
  }
  background-color: #f1efef;
  h2 {
    font-weight: lighter;
    margin-top: 0.5em;
  }
  h2::after {
    content: '';
    display: block;
    width: 18%;
    margin: 0.9em auto;
    height: 1px;
    background-color: gray;
  }
  hr {
    display: block;
    width: 10%;
  }
  .text-box {
    p {
      width: 37%;
      line-height: 2em;
      font-weight: 300;
    }
  }
  .doc-box {
    width: 70%;
    margin: 0 auto;
    .doc-card {
      padding: 0;
      margin: 3em 0 6em 0;
      flex-basis: calc((100% / 3 - 2em));
      img {
        width: 100%;
      }
      .card-text {
        background-color: white;
        padding: 2em 1.5em;
        h3 {
          font-size: 1em;
          font-weight: lighter;
          margin-top: 1em;
        }
        h4 {
          font-weight: lighter;
          font-size: 0.9em;
          margin-bottom: 2em;
        }
        p {
          font-size: 0.9em;
          line-height: 2.1em;
          color: #7c858f;
        }
      }
    }
  }
}
</style>
