<template>
  <div class="p-20 bg-blue-100">
    <h3 class="text-blue-300 mb-4 text-sm font-bold">
    Simple POST Request with Error Handling
    </h3>
    <div class="bg-white p-6 rounded-lg shadow-lg">
      <h2 class="text-2xl font-bold mb-2 text-gray-800">Here is what you posted</h2>
      <p class="text-gray-700 text-red-500">Error message: <span class="text-red-300" > {{errorMessage}}</span></p>
    </div>
  </div>
<!-- card with image -->
</template>

<script>
import axios from 'axios';

export default {
  name: "post-request-error-handling",
 data() {
    return {
      articleId: null,
      errorMessage: null
    };
  },
  created() {
    // POST request using axios with error handling
    const article = { title: "Vue POST Request Example" };
    axios.post("https://reqres.in/invalid-url", article)
      .then(response => this.articleId = response.data.id)
      .catch(error => {
        this.errorMessage = error.message;
        console.error("There was an error!", error);
      });
  }
};
</script>
