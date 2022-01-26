<template>
  <div class="test">
    <div class="row justify-content-center text-center text-box">
      <h2 class="">
        Make An Appointment
      </h2>
      <p>
        Sed ut perspiciatis unde omnis iste natus error sit voluptatem
        accusantium dolorumque laudantium,
        totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae
      </p>
    </div>
    <div class="row form-box">
      <div class="col ps-0">
        <input
          type="text"
          class="form-control"
          placeholder="Name*"
          aria-label="Name"
        >
      </div>
      <div class="col pe-0">
        <input
          type="email"
          class="form-control"
          placeholder="Email*"
          aria-label="Email"
        >
      </div>
    </div>
    <div class="row form-box">
      <div class="col ps-0">
        <input
          type="tel"
          class="form-control"
          placeholder="Phone Number"
          aria-label="Phone Number"
        >
      </div>
      <div class="col pe-0">
        <input
          type="date"
          class="form-control"
          placeholder="Appointment Date"
          aria-label="Appointment Date"
        >
      </div>
    </div>
    <div class="row form-box">
      <textarea
        id="exampleFormControlTextarea1"
        class="form-control"
        rows="3"
        placeholder="How can we help?*"
      />
    </div>
    <div class="btninput">
      <button
        type="button"
        class="btn btn-primary btn-lg text-uppercase"
      >
        Make an appointment
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'InputForm',
};
</script>

<style lang="scss" scoped>
@import "~bootstrap/scss/bootstrap";
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
.text-box {
  p {
    width: 38%;
    line-height: 2em;
    font-weight: 100;
  }
}
.form-box {
  width: 46%;
  margin: 0 auto;
  input {
    background-color: transparent;
    color: white;
    font-size: 1.3em;
    padding: 0.5em;
  }
  textarea {
    background-color: transparent;
    color: white;
    font-size: 1.3em;
  }
}
.btninput {
  width: 46%;
  margin: 0 auto;
  button {
    width: 100%;
    font-size: 1.2em;
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
</style>
