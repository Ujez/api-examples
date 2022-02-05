<template>
  <div>
    <post-request/>
    <!-- <get-request/> -->
   <!-- <get-request-async-await/> -->
    <!-- <get-request-error-handling/> -->
     <!-- <get-request-set-headers/> -->
  </div>
</template>

<script>

import PostRequest from "./components/postrequests/PostRequest.vue";
// import PostRequestAsyncAwait from "./PostRequestAsyncAwait";
// import PostRequestErrorHandling from "./PostRequestErrorHandling";
// import PostRequestSetHeaders from "./PostRequestSetHeaders";
// import GetRequest from "./components/GetRequest.vue";
// import GetRequestAsyncAwait from "./components/GetRequestAsyncAwait.vue";
// import   GetRequestErrorHandling from "./components/GetRequestErrorHandling.vue";
// import GetRequestSetHeaders from "./components/GetRequestSetHeaders.vue";

export default {
  name: "app",
  components: {
    PostRequest,
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
