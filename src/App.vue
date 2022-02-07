<template>
  <div>
    <swapi/>
    <!-- <post-request/> -->
       <!-- <post-request-async-await/> -->
    <!-- <post-request-error-handling/> -->
    <!-- <post-request-set-headers/> -->
    <!-- <get-request/> -->
   <!-- <get-request-async-await/> -->
    <!-- <get-request-error-handling/> -->
     <!-- <get-request-set-headers/> -->
  </div>
</template>

<script>
import swapi from "./components/swapi.vue"
// import PostRequest from "./components/postrequests/PostRequest.vue";
// import PostRequestAsyncAwait from "./components/postrequests/PostRequestAsyncAwait.vue";
// import PostRequestErrorHandling from "./components/postrequests/PostRequestErrorHandling.vue";
// import PostRequestSetHeaders from "./components/postrequests/PostRequestSetHeaders.vue";
// import GetRequest from "./components/GetRequest.vue";
// import GetRequestAsyncAwait from "./components/GetRequestAsyncAwait.vue";
// import   GetRequestErrorHandling from "./components/GetRequestErrorHandling.vue";
// import GetRequestSetHeaders from "./components/GetRequestSetHeaders.vue";

export default {
  name: "app",
  components: {
    swapi
    // PostRequest,
    // PostRequestAsyncAwait,
    // PostRequestErrorHandling,
    // PostRequestSetHeaders
    // GetRequest,
  //  GetRequestAsyncAwait
    // GetRequestErrorHandling,
    //  GetRequestSetHeaders
    
  }
};
</script>
