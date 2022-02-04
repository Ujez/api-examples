<template>
  <div>
    <!-- <get-request/> -->
   <get-request-async-await/>
    <!-- <get-request-error-handling/> -->
  </div>
</template>

<script>
// import GetRequest from "./components/GetRequest.vue";
import GetRequestAsyncAwait from "./components/GetRequestAsyncAwait.vue";
// import   GetRequestErrorHandling from "./components/GetRequestErrorHandling.vue";

export default {
  name: "app",
  components: {
    // GetRequest,
   GetRequestAsyncAwait
    // GetRequestErrorHandling,
  }
};
</script>
