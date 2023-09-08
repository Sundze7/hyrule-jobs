<template>
  <div class="app">
    <JobList :jobs="jobs" />
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";
import "./assets/global.css";
import Job from "./types/Job";
import JobList from "./components/JobList.vue";

export default defineComponent({
  name: "App",
  components: { JobList },
  setup() {
    const jobs = ref<Job[]>([
      {
        title: "farm worker",
        location: "lon lon ranch",
        salary: 300000,
        id: "1",
      },
      {
        title: "fisher",
        location: "seaport",
        salary: 30000,
        id: "2",
      },
      {
        title: "worker",
        location: "tranch",
        salary: 300000,
        id: "3",
      },
    ]);

    return { jobs };
  },
});
</script>
