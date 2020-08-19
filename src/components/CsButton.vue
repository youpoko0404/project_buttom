<template>
  <div>
    <button v-on:click="upFunction" class="btn btn-info ml-3">LIKE</button>
    <button v-on:click="downFunction" class="btn btn-primary ml-3">DISLIKE</button>
    <button v-on:click="LoveFunction" class="btn btn-success ml-3">LOVE</button>
    <button v-on:click="HateFunction" class="btn btn-danger ml-3">HATE</button>
    <button v-on:click="ResetFunction" class="btn btn-warning ml-3">RESET</button>
  </div>
</template>
<script>
export default {
  data: function () {
    return {
      counter: 0,
    };
  },

  methods: {
    upFunction: function () {
      this.counter += 1;
      this.$emit("cc", this.counter);
    },

    downFunction: function () {
      this.counter -= 1;
      this.$emit("cc", this.counter);
    },

    LoveFunction: function () {
      this.counter += 10;
      this.$emit("cc", this.counter);
    },

    HateFunction: function () {
      this.counter -= 10;
      this.$emit("cc", this.counter);
    },

    ResetFunction: function () {
      this.counter = 0;
      this.$emit("cc", this.counter);
    },
  },
};
</script>
<style>
</style>