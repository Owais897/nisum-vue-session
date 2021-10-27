<template>
  <div>
    <button @click="$emit('clicked')">
      clicked
    </button>
    <button @click="$emit('clickedPayload', 1)">
      clicked with payload
    </button>
    <button @dblclick="doubleClicke">
      doubleclicked
    </button>
  </div>
</template>

<script>
export default {
  name: "Child",
  props: {
    msg: String,
  },
  data() {
    return {
      text: "",
    };
  },
  methods: {
    doubleClicke() {
      this.$emit("doubleclicked");
    },
  },
};
</script>

<style></style>
