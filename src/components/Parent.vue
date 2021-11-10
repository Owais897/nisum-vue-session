<template>
  <div>
    <Child
      @clicked="buttonclicked"
      @clickedPayload="clickedPayload"
      @doubleclicked="doubleclicked"
    />
    <PropsExample :value="value" />
  </div>
</template>

<script>
import Child from "./Child.vue";
import PropsExample from "./PropsExample.vue";
export default {
  data() {
    return {
      value: "owais is send in props",
    };
  },
  components: {
    Child,
    PropsExample,
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
