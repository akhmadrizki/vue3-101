<template>
  <div class="app">
    <Joblist :jobs="jobs" />
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";
import Joblist from "./components/Joblist.vue";
import Job from "./types/Job";

export default defineComponent({
  name: "App",
  components: { Joblist },
  setup() {
    // const state = reactive({
    //   name: "Link",
    //   age: 21 as number,
    // });
    // state.name = "Yoga Ganteng";
    // return { ...toRefs(state) };
    // const name = ref("Link");
    // const age = ref(21);
    // return { name, age };

    const jobs = ref<Job[]>([
      { title: "Daily Worker", location: "Nusa Dua", salary: 100000, id: "1" },
      { title: "Tukang Sapu", location: "Kuta", salary: 100000, id: "2" },
      { title: "Waitress", location: "Denpasar", salary: 100000, id: "3" },
      { title: "House Keeping", location: "Ubud", salary: 100000, id: "4" },
    ]);

    return { jobs };
  },
});
</script>

<style></style>
