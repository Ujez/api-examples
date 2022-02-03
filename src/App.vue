<template>
  <div>
    <h3 class="p-3 text-center">Vue HTTP GET Requests with Fetch</h3>
    <!-- <get-request/> -->
   <get-request-async-await/>
  </div>
</template>

<script>
// import GetRequest from "./components/GetRequest.vue";
import GetRequestAsyncAwait from "./components/GetRequestAsyncAwait.vue";

export default {
  name: "app",
  components: {
   GetRequestAsyncAwait
  }
};
</script>
