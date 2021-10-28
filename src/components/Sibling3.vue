<template
  ><div>
    SIBLING 3
    {{ list.reverse() }}
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
};
</script>

<style></style>
