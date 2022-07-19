<template>
  <h1>{{ title }}</h1>
  <h3>{{ id }}</h3>
</template>

<script>
export default {
  props: ["id"],
  data() {
    return {
      title: "Job Details",
    };
  },
};
</script>

<style>
</style>