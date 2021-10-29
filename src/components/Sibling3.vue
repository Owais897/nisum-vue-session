<template
  ><div>
    SIBLING 3
    {{ list }}
  </div>
</template>

<script>
export default {
  name: "Child2",
  data() {
    return {
      list: [],
    };
  },
  methods: {
    updateList() {
      this.$root.$emit("updateWordList", this.word);
      this.word = "";
    },
  },
  created() {
    this.$root.$on("updateWordList", (word) => {
      this.list.push(word);
    });
  },
  watch: {
    list: {
      handler(a, b) {
        console.log("a: ", a);
        console.log("b: ", b);
      },
      deep: true,
    },
  },
};
</script>

<style></style>
