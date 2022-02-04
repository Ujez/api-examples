<template>
  <div class="card text-center m-3">
    <h5 class="card-header"></h5>
    <div class="card-body"></div>
  </div>
  <!-- card with no image -->

<div class="p-20 bg-blue-100">
  <h3 class="text-blue-300 mb-4 text-sm font-bold">
    GET Request with Error Handling
  </h3>
  <div class="bg-white p-6 rounded-lg shadow-lg">
    <h2 class="text-2xl font-bold mb-2 text-gray-800">Error message: {{errorMessage}}</h2>
    <p class="text-gray-700 text-red-500">Check you console to see the full message!</p>
  </div>
</div>

<!-- card with image -->
</template>

<script>
import axios from 'axios';

export default {
  name: "get-request-error-handling",
  data() {
    return {
      totalVuePackages: null,
      errorMessage: null
    };
  },
  created() {
      // GET request using axios with error handling
  axios.get("https://api.npms.io/v2/invalid-url")
    .then(response => this.totalVuePackages = response.data.total)
    .catch(error => {
      this.errorMessage = error.message;
      console.error("There was an error!", error);
    });
  }
};
</script>
