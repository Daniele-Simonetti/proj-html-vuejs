<template>
  <header>
    <!-- creo un haeder con link dinamici -->
    <div class="container-fluid">
      <div class="row nav-bar">
        <div class="col-6 logo">
          <img
            src="../assets/images/medical_logo_2x_light.png"
            alt="logo-light"
          >
        </div>
        <div class="col-6">
          <ul class="nav justify-content-end align-items-center flex-nowrap">
            <li
              v-for="(link, index) in links"
              :key="index"
              class="nav-item text-uppercase"
            >
              <a
                :href="link.href"
                class="nav-link"
              >{{ link.name }}</a>
            </li>
            <li>
              <button
                type="button"
                class="btn btn-primary btn-lg text-uppercase"
              >
                Make appointment
              </button>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header',
  props: {
    links: {
      type: Array,
      default() {
        return [];
      },
    },
  },
};
</script>

<style lang="scss" scoped>
header {
  // background-image: url('../assets/images/header-image-homepage.jpg');
  position: absolute;
  left: 0;
  right: 0;
  margin: auto;

  .nav-bar {
    padding: 1em 0;
  }
  .logo {
    img {
      width: 35%;
    }
  }
  ul {
    li {
      a {
        color: white;
        padding: 0 1.1em;
        font-size: 0.8em;
        &:hover,
        &:active,
        &:focus {
          color: #39afbb;
        }
      }
      button {
        font-size: 0.9em;
        background-color: #39afbb;
        border: 0;
        border-radius: 0.2rem;
        padding: 0.5em 1.8em;
        &:active,
        &:focus {
          background-color: #39afbb;
          border: 0;
          box-shadow: 0 0 0 0;
        }
      }
    }
  }
}

</style>
