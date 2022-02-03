<template>
  <div class="card text-center m-3">
    <h5 class="card-header">GET Request with Async/Await</h5>
    <div class="card-body">Total vue packages: {{totalVuePackages}}</div>
  </div>
</template>

<script>
export default {
  name: "get-request-async-await",
  data() {
    return {
      totalVuePackages: null
    };
  },
  async created() {
    // GET request using fetch with async/await
    const response = await fetch("https://api.npms.io/v2/search?q=vue");
    const data = await response.json();
    this.totalVuePackages = data.total;
  }
};
</script>
