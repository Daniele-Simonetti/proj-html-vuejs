/* eslint-disable max-len */
/* eslint-disable vue/multiline-html-element-content-newline */
<template>
  <main>
    <!-- creo il jumbo con lo sfondo che copre anche l'header -->
    <div class="jumbo">
      <div class="row">
        <div class="col-4  test">
          <h1>Caring <span>For Life</span></h1>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit.
            Error, optio. Et commodi ex aut mollitia animi.
          </p>
        </div>
      </div>
    </div>
  </main>
</template>

<script>
export default {
  name: 'Main',
};
</script>

<style lang="scss" scoped>
.jumbo {
  background-image: url('../assets/images/header-image-homepage.jpg');
  background-repeat: no-repeat;

  // height: 865px;
  .test {
    margin-top: 290px;
    margin-left: 480px;
    margin-bottom: 460px;
  }
}
</style>
