<template>
  <Child
    @clicked="buttonclicked"
    @clickedPayload="clickedPayload"
    @doubleclicked="doubleclicked"
  />
</template>

<script>
import Child from "./Child.vue";
export default {
  components: {
    Child,
  },
  methods: {
    buttonclicked() {
      console.log("clicked button call");
    },
    clickedPayload(p) {
      console.log("clickedPayload: ", p);
    },
    doubleclicked() {
      console.log("doubleclicked");
    },
  },
};
</script>

<style></style>
