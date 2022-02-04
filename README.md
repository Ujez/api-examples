# Vue 3 + Vite + Simple GET Request + Tailwindcss


# HOW IT WORKS
This sends a GET request from Vue to an invalid url on the npm api then assigns the error to the _errorMessage_ component data property and logs the error to the console.

The _fetch()_ function will automatically throw an error for network errors but not for HTTP errors such as 4xx or 5xx responses. For HTTP errors we can check the _response.ok_ property to see if the request failed and reject the promise ourselves by calling _return Promise.reject(error);_. This approach means that both types of failed requests - network errors and http errors - can be handled by a single _catch()_ block.


This template should help get you started developing with Vue 3 in Vite. The template uses Vue 3 `<script setup>` SFCs, check out the [script setup docs](https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup) to learn more.


## Recommended IDE Setup

- [VSCode](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=johnsoncodehk.volar)
