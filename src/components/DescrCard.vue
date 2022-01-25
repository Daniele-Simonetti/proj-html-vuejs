<template>
  <div class="row justify-content-center text-center text-box">
    <img
      :src="require(`../assets/images/icon-5.png`)"
      alt="doc-logo"
      class="doc-logo"
    >
    <h2 class="text-uppercase">
      {{ description.title }}
    </h2>
    <p>
      {{ decription.text }}
    </p>
  </div>
</template>

<script>
export default {
  name: 'DescrCard',
  props: {
    description: {
      type: Array,
      default() {
        return [];
      },
    },
  },
};
</script>

<style lang="scss" scoped>
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
      font-weight: 100;
    }
  }
}
</style>
