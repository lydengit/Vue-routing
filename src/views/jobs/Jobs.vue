<template>
  <h1>{{ title }}</h1>
  <div v-for="job in jobs" :key="job.id">
    <router-link :to="{ name: 'jobDetails', params: { id: job.id } }">
      <h3>{{ job.title }}</h3>
    </router-link>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: "Jobs",
      jobs: [
        { title: "Web designer", id: 1, details: "Web designer job" },
        { title: "Vue designer", id: 2, details: "Vue developer job" },
        { title: "React designer", id: 3, details: "React designer job" },
      ],
    };
  },
};
</script>

<style scoped>
  a:hover {
    color: cornflowerblue;
  }
</style>