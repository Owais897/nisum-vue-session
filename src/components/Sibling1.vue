<template>
  <div>
    Sibling 1 where event is trigger
    <input type="text" v-model="word" @keypress.enter="updateList" />
  </div>
</template>

<script>
export default {
  name: "Child1",
  data() {
    return {
      word: "",
    };
  },
  methods: {
    updateList() {
      this.$root.$emit("updateWordList", this.word);
      this.word = "";
    },
  },
};
</script>

<style></style>
