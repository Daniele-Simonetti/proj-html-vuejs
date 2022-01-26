<template>
  <footer>
    <div class="row startFooter">
      <div class="col-4 mainPartFoot">
        <img
          :src="require(`../assets/images/medical_logo_1x_dark.png`)"
          alt="logo-nero"
        >
        <p>
          Sed ut perspiciatis unde omnis iste
          natus error sit voluptatem accusantium dolemue launti totam aperiam,
          eaque ipsa quae abillo.
          Invente veriatis et quasi architecto beatae luptatem accusantium,
          remaperiamsiat.
          Voluptatem accusest etsium doloremque laudaien.
          Lorem ipsum sits dolores ets unser.
        </p>
        <h4 class="text-uppercase">
          Learn more about us
        </h4>
        <i class="fab fa-facebook-square facebook" />
        <i class="fab fa-twitter-square twitter" />
        <i class="fab fa-youtube-square youtube" />
        <i class="fab fa-instagram-square instagram" />
      </div>
      <div class="col-4 contactInfos">
        <h4 class="text-uppercase">
          Contact information
        </h4>
        <p><i class="fas fa-map-marker-alt" /> 121 King Street, London United Kingdom</p>
        <p><i class="fas fa-phone" /> 1.800.458.556</p>
      </div>
      <div class="col-4 medicalDep">
        <h4 class="text-uppercase">
          Medical departments
        </h4>
        <ul
          class="list-unstyled"
        >
          <li
            v-for="(depart, index) in medDepartment"
            :key="index"
          >
            <i class="fas fa-chevron-right blueBGIcon rounded-circle" /> {{ depart }}
          </li>
          <button
            type="button"
            class="btn btn-primary btn-lg text-uppercase"
          >
            View our departments
          </button>
        </ul>
      </div>
    </div>
    <div class="row end">
      <div class="col-6">
        <ul class="list-inline">
          <li class="list-inline-item">
            <i class="far fa-copyright" /> Copyright 2012 - 2020
          </li>
          <li class="list-inline-item">
            Avada Theme by <span>Theme Fusion</span>
          </li>
          <li class="list-inline-item">
            All Rights Reserved
          </li>
          <li class="list-inline-item lastItem">
            Powered by <span>WordPress</span>
          </li>
        </ul>
      </div>
      <div class="col-6 text-end">
        <a
          href="#makeApp"
          class="text-decoration-none"
        >
          <button>
            <i class="fas fa-chevron-up" />
          </button>

        </a>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
  data() {
    return {
      medDepartment: [
        'Cardiology',
        'Pediactrics',
        'Diabetes Care',
        'Pre-natel Care',
        'Ultrasound Echocardiogram',
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.startFooter {
  padding: 3em;
  .mainPartFoot {
    p {
      font-size: 0.7em;
      line-height: 2.3em;
      font-weight: 100;
      margin-top: 1em;
      margin-bottom: 1em;
      border-bottom: 1px solid lightgray;
      padding-bottom: 2em;
    }
    h4 {
      font-weight: 100;
    }
    i {
      font-size: 2em;
      margin-right: 0.3em;
    }
    i.facebook {
      color: #385898;
    }
    i.twitter {
      color: #3ba5bd;
    }
    i.youtube {
      color: #cc201f;
    }
    i.instagram {
      color: #0764AD;;
    }
  }
}
.contactInfos {
  h4 {
    margin: 0;
    &::after {
      content: '';
      background-color: #449ebf;
      margin: 0.5em 0;
      height: 2px;
      width: 10%;
      display: block;
    }
  }
  p {
    margin: 0.5em 0;
    font-weight: 100;
  }
  i {
    color: #449ebf;
    padding-right: 0.5em;
  }
}
.medicalDep {
  h4 {
    margin: 0;
    &::after {
      content: '';
      background-color: #449ebf;
      margin: 0.5em 0;
      height: 2px;
      width: 10%;
      display: block;
    }
  }
  li {
    font-weight: 100;
  }
  i.blueBGIcon {
    background-color: #39afbb;
    color: white;
    font-size: 0.7em;
    padding: 0.8em;
    margin: 0.5em 0.5em 0.5em 0;
  }
  button {
    margin-top: 3em;
    font-size: 1em;
    font-weight: 500;
    color: black;
    background-color: transparent;
    border: 1px solid black;
    padding: 0.5em 2.5em;
    border-radius: 0;
  }

}
  .end {
    background-color: #f1efef;
    padding: 1.5em 3em;
    ul {
      font-size: 0.8em;
      li {
        padding-right: 0.5em;
        margin: 0.3em;
        border-right: 1px solid black;
      }
      .lastItem {
        border-right: 0;
      }
    }
    button {
      background-color: #3d4954;
      color: white;
    }
  }
</style>
