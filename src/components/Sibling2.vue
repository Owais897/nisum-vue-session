<template
  ><div>
    SIBLING 2
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

  created() {
    this.$root.$on("updateWordList", (word) => {
      this.list.push(word);
    });
  },
};
</script>

<style></style>
