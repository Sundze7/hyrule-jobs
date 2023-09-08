<template>
  <div class="job-list">
    <li v-for="job in jobs" :key="job.id">
      <h2>{{ job.title }} in {{ job.location }}</h2>
      <div class="salary">
        <p>{{ job.salary }} FCFA</p>
      </div>
      <div class="description">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Omnis provident
        enim incidunt repellendus illo, neque rerum pariatur iure aut deserunt
        ducimus tempora, fuga eius nesciunt?
      </div>
    </li>
  </div>
</template>

<script lang="ts">
import { PropType, defineComponent } from "vue";
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
