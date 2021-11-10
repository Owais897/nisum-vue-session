<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png" /> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App" /> -->
    <!-- <HandlingInputs /> -->
    <!-- <Form /> -->
    <Parent />
    <!-- <Sibling1 />
    <Sibling2 />
    <Sibling3 /> -->
    <!-- <Slots /> -->
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
// import HandlingInputs from "./components/handlingInputs.vue";
// import Form from "./components/Form.vue";
import Parent from "./components/Parent.vue";
// import Sibling1 from "./components/Sibling1.vue";
// import Sibling2 from "./components/Sibling2.vue";
// import Sibling3 from "./components/Sibling3.vue";
// import Slots from "./components/Slots.vue";

export default {
  name: "App",
  components: {
    // HelloWorld,
    // HandlingInputs,
    // Form,
    Parent,
    // Sibling1,
    // Sibling2,
    // Sibling3,
    // Slots,
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
