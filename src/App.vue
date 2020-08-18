<template>
  <div id="app">
    <HelloWorld msg="เลือกเลยนะครับ" />
    <hr />
    <div class="row">
      <div class="col-6">
        <img alt="Vue logo" src="./assets/1.jpg" />
        <h1>{{total1}}</h1>
      </div>
      <div class="col-6">
        <img alt="Vue logo" src="./assets/2.jpg" />
        <h1>{{total2}}</h1>
      </div>
      <div class="col-6">
        <CSButton @cc="sum" />
      </div>
      <div class="col-6">
        <CSButton @cc="sum1" />
      </div>
    </div>
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
  color: #2c3e50;
  margin-top: 60px;
}
</style>
