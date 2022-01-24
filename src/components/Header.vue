<template>
  <header>
    <div class="container">
      <div class="row">
        <div class="col-6">
          logo
        </div>
        <div class="col-6">
          <ul class="nav">
            <li
              v-for="(link, index) in links"
              :key="index"
              class="nav-item"
            >
              <a
                :href="link.href"
                class="nav-link"
              >{{ link.name }}</a>
            </li>
            <li>
              <button
                type="button"
                class="btn btn-primary btn-lg"
              >
                Make an appointment
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

<style>

</style>
