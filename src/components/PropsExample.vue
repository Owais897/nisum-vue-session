<template>
  <div>
    {{ value }}
  </div>
</template>

<script>
export default {
  //   props: ["value"],
  //   props: {
  //     value: String,
  //   },
  props: {
    value: {
      //   required: true,
      //   default: "owais default string",
      type: String,
      default: function() {
        return "owais is send from default function";
      },
      validator: function(value) {
        return value.length > 0;
      },
    },
  },
};
</script>

<style></style>
