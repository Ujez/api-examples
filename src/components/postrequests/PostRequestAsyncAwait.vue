<template>
  <div class="p-20 bg-blue-100">
    <h3 class="text-blue-300 mb-4 text-sm font-bold">
 GET Request with Async/Await
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
  name: "get-request-async-await",
  data() {
    return {
      totalVuePackages: null
    };
  },
  async created() {
      // GET request using axios with async/await
  const response = await axios.get("https://api.npms.io/v2/package/react");
  this.totalVuePackages = response.data.evaluation.quality;
  }
};
</script>
