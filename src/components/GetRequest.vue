<template>
  <div class="card text-center m-3">
    <h5 class="card-header"></h5>
    <div class="card-body"></div>
  </div>
  <div class="p-20 bg-blue-100">
  <h3 class="text-blue-300 mb-4 text-sm font-bold">
   Simple GET Request
  </h3>
  <div class="bg-white p-6 rounded-lg shadow-lg">
    <h2 class="text-2xl font-bold mb-2 text-gray-800">Here is what you requested</h2>
    <p class="text-gray-700 text-red-500">Total vue packages: <span class="text-blue-300" > {{totalVuePackages}}</span></p>
  </div>
</div>
</template>

<script>
import axios from 'axios';

export default {
  name: "get-request",
  data() {
    return {
      totalVuePackages: null,
    };
  },
  created() {
    // Simple GET request using fetch
    // fetch("https://api.npms.io/v2/search?q=vue")
    //   .then(response => response.json())
    //   .then(data => (this.totalVuePackages = data.total));
        // Simple GET request using axios
    axios.get("https://api.npms.io/v2/search?q=vue")
      .then(response => this.totalVuePackages = response.data.total);
  },

};
</script>
