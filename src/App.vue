<template>
  <div class="app">
    <p>{{ name }} - {{ age }}</p>
    <button @click="changeName('yoga')">Change Name</button>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "App",
  components: {},
  data() {
    return {
      name: "Link",
      age: 21 as number,
    };
  },
  methods: {
    changeName(name: string) {
      this.name = name;
      return name;
    },
  },
});
</script>

<style></style>
