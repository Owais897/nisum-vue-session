<template>
  <div>
    {{ text }}
    <input v-model="text" type="text" />
  </div>
</template>

<script>
export default {
  name: "handlingInputs",
  props: {
    msg: String,
  },
  data() {
    return {
      text: "",
    };
  },
};
</script>

<style></style>
