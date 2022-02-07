<template>
<div>
     <button  @click="getAllStarWarsFilms" class="mt-5 mx-5 h-10 px-6 font-semibold rounded-md bg-black text-white active:bg-yellow-500" type="submit">
          show starwars films
    </button>
        <div class="bg-white rounded-lg shadow lg:w-1/3">
            <ul class="divide-y divide-gray-100">
                <li v-for="starwarsallfilm in starwarsallfilms.results" :key="starwarsallfilm.title"
                class="p-3 hover:bg-blue-600 hover:text-blue-200">
                    {{ starwarsallfilm.title }}
                </li>
            </ul>
        </div> 
</div>
       
</template>

<script>
import axios from 'axios';

export default {
    name: "starwars",
      data() {
        return {
            starwarsallfilms:[]
        }
    },
    methods:{
        getAllStarWarsFilms(){
           axios.get("https://swapi.dev/api/films/")
      .then(response => this.starwarsallfilms = response.data);
        }
    },
}
</script>

<style>

</style>