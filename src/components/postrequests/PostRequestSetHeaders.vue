<template>
  <div class="p-20 bg-blue-100">
    <h3 class="text-blue-300 mb-4 text-sm font-bold">
   POST Request with Set Headers
    </h3>
    <div class="bg-white p-6 rounded-lg shadow-lg">
      <h2 class="text-2xl font-bold mb-2 text-gray-800">Here is what you posted</h2>
      <p class="text-gray-700 text-red-500">Returned Id: <span class="text-red-300" > {{articleId}}</span></p>
    </div>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  name: "post-request-set-headers",
  data() {
    return {
     articleId: null,
      errorMessage: null
    };
  },
created() {
  // POST request using axios with set headers
  const article = { title: "Vue POST Request Example" };
  const headers = { 
    "Authorization": "Bearer my-token",
    "My-Custom-Header": "foobar"
  };
  axios.post("https://reqres.in/api/articles", article, { headers })
    .then(response => this.articleId = response.data.id);
}
};
</script>
