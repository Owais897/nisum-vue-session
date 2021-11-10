<template>
  <div>
    <h2>
      slots are used to add things dynamically
    </h2>
    <SlotE1> parentText </SlotE1>
    <SlotE1> <button>owais</button> </SlotE1>
    <SlotE1> <input type="text" /> </SlotE1>
    <SlotE2>
      <!-- this will go in default -->
      <p>A paragraph for the main content.</p>
      <p>And another one.</p>

      <template #footer>
        <h3>Here's some contact info</h3>
      </template>

      <template #header>
        <h1>Here might be a page title</h1>
      </template>
    </SlotE2>
    <h3>
      scoped slot examples
    </h3>
    <SlotE3>
      <template #scoped> </template>
    </SlotE3>
    <SlotE3>
      <template #scoped="user">
        {{ user.user2.name }}
      </template>
    </SlotE3>
    <SlotE3>
      <template #scoped="{user2}">
        {{ user2.name }}
      </template>
    </SlotE3>
  </div>
</template>

<script>
import SlotE1 from "./SlotE1.vue";
import SlotE2 from "./SlotE2.vue";
import SlotE3 from "./SlotE3.vue";
export default {
  name: "Slots",
  components: {
    SlotE1,
    SlotE2,
    SlotE3,
  },
};
</script>

<style></style>
