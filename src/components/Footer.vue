<template>
  <div class="row">
    <div class="col-4">
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
      <i class="fab fa-youtube-square" />
      <i class="fab fa-instagram-square instagram" />
    </div>
    <div class="col-4">
      <h4 class="text-uppercase">
        Contact information
      </h4>
      <p><i class="fas fa-map-marker-alt" /> 121 King Street, London United Kingdom</p>
      <p><i class="fas fa-phone" /> 1.800.458.556</p>
    </div>
    <div class="col-4">
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
i.blueBGIcon {
  background-color: #39afbb;
  color: white;
  font-size: 0.7em;
  padding: 0.8em;
}
button {
  font-size: 0.7em;
  font-weight: 500;
  color: black;
  background-color: transparent;
  border: 1px solid black;
  padding: 0.5em 2em;
  border-radius: 0;
}

</style>
