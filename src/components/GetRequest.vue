<template>
  <div class="card text-center m-3">
    <h5 class="card-header">Simple GET Request</h5>
    <div class="card-body">Total vue packages: {{totalVuePackages}}</div>
  </div>
</template>

<script>
export default {
  name: "get-request",
  data() {
    return {
      totalVuePackages: null,
    };
  },
  created() {
    // Simple GET request using fetch
    fetch("https://api.npms.io/v2/search?q=vue")
      .then(response => response.json())
      .then(data => (this.totalVuePackages = data.total));
  },

};
</script>
