<template
  ><div>
    SIBLING 3
    {{ list }}
    <br />
    {{ obj }}
  </div>
</template>

<script>
export default {
  name: "Child2",
  data() {
    return {
      list: [],
      obj: {
        name: "owais",
        age: {
          value: 10,
        },
      },
    };
  },

  created() {
    this.$root.$on("updateWordList", (word) => {
      this.list.push(word);
    });
    setInterval(() => {
      this.obj.age.value++;
    }, 3000);
  },
  watch: {
    obj: {
      handler(a, b) {
        console.log("a: ", a);
        console.log("b: ", b);
      },
      deep: true,
      immediate: true,
    },
  },
};
</script>

<style></style>
