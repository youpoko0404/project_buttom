<template>
  <div id="app">
    <section class="ftco-about ftco-section" id="about">
      <HelloWorld msg="Please select the one you like." />
      <hr />
      <div class="container">
        <div class="row d-flex no-gutters">
          <div class="col-md-6 col-lg-6 d-flex">
            <div class="img-about img d-flex align-items-stretch">
              <div
                class="img img-video d-flex align-self-stretch align-items-center"
                style="background-image:url(./assets/img/1.jpg);"
              ></div>
            </div>
          </div>
          <div class="col-md-6 col-lg-6 pl-md-5">
            <div class="heading-section ftco-animate">
              <h2 class="mb-4">Prayut Chan-o-cha</h2>
              <p></p>
              <div class="d-flex w-100">
                <div
                  class="img img-about-2 mr-2"
                  style="background-image: url(./assets/img/pra4.jpg);"
                ></div>
                <div
                  class="img img-about-2 ml-2"
                  style="background-image: url(./assets/img/pra3.jpg);"
                ></div>
              </div>
              <div class="text">
                <h1>Score {{total1}}</h1>
                <CSButton @cc="sum" />
              </div>
            </div>
          </div>
        </div>
      </div>
      <hr />
      <hr />
      <div class="container">
        <div class="row d-flex no-gutters">
          <div class="col-md-6 col-lg-6 d-flex pl-md-5">
            <div class="heading-section ftco-animate">
              <h2 class="mb-4">Pigkaploy</h2>
              <p></p>
              <div class="d-flex w-100">
                <div
                  class="img img-about-2 mr-2"
                  style="background-image: url(./assets/img/pink1.jpg);"
                ></div>
                <div
                  class="img img-about-2 ml-2"
                  style="background-image: url(./assets/img/pink2.jpg);"
                ></div>
              </div>
              <div class="text">
                <h1>Score {{total2}}</h1>
                <CSButton @cc="sum1" />
              </div>
            </div>
          </div>
          <div class="col-md-6 col-lg-6 d-flex">
            <div class="img-about img d-flex align-items-stretch">
              <div
                class="img d-flex align-self-stretch align-items-center"
                style="background-image:url(./assets/img/2.jpg);"
              ></div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import CSButton from "./components/CsButton";

export default {
  name: "App",
  components: {
    HelloWorld,
    CSButton,
  },

  data: function () {
    return {
      total1: 0,
      total2: 0,
    };
  },

  methods: {
    sum(counterValue) {
      this.total1 = counterValue;
    },
    sum1(counterValue) {
      this.total2 = counterValue;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
</style>
