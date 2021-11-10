<template>
  <div>
    <br />
    <slot name="scoped" :user1="user1" :user2="user2"> {{ user1.name }}</slot>
  </div>
</template>

<script>
export default {
  name: "Slots3",
  data() {
    return {
      user1: {
        name: "owais",
      },
      user2: {
        name: "muhammad owais",
      },
    };
  },
};
</script>

<style></style>
