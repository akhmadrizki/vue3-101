<template>
  <div class="job-list">
    <ul>
      <li v-for="job in jobs" :key="job.id">
        <h2>{{ job.title }} in {{ job.location }}</h2>
        <div class="salary">
          <p>Rp. {{ job.salary }}</p>
        </div>
        <div class="description">
          <p>
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Cum animi
            est in quisquam ab fugiat nostrum corrupti quidem quas. Dolor
            consequatur dolores omnis quos sunt culpa magnam aut. Dolore nemo
            vero laborum, nihil est repudiandae iusto expedita eaque atque fuga
            quis, numquam esse natus culpa qui officiis architecto provident
            inventore.
          </p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script lang="ts">
import { defineComponent, PropType } from "vue";
import Job from "@/types/Job";

export default defineComponent({
  props: {
    jobs: {
      required: true,
      type: Array as PropType<Job[]>,
    },
  },
});
</script>

<style scoped>
.job-list {
  max-width: 960px;
  margin: 40px auto;
}

.job-list ul {
  padding: 0;
}

.job-list li {
  list-style-type: none;
  background: white;
  padding: 16px;
  margin: 16px 0;
  border-radius: 4px;
}

.job-list h2 {
  margin: 0 0 10px;
  text-transform: capitalize;
}

.salary {
  display: flex;
}

.salary img {
  width: 30px;
}

.salary p {
  color: #17bf66;
  font-weight: bold;
  margin: 10px 4px;
}
</style>
