<template>
<div>
    <div v-if="show_country">
            <div class="mx-10 flex items-center justify-start  "><a href="#" @click.prevent="showCountries" 
        class="bg-orange-400 py-3 px-8 mt-4 rounded text-sm 
        text-gray-200 font-semibold hover:bg-orange-700 items-center"> All Countries</a></div>
        <div v-for="c in country" :key="c">
            <div class="p-10 grid grid-cols-1 sm:grid-cols-1 md:grid-cols-3 
                lg:grid-cols-3 xl:grid-cols-4 gap-5">
                <!--Card 1-->
                <div class="rounded overflow-hidden shadow-lg" >
                <img class="w-full" :src="c.flag" alt="Mountain">
                <div class="px-6 py-4">
                    <div class="font-bold text-xl mb-2">{{c.name}}</div>
                    <p class="text-gray-700 text-base">
                Capital City: {{c.capital}}
                    </p>
                </div>
                <div class="px-6 pt-4 pb-2">
                    <span class="inline-block bg-gray-200 rounded-full px-3 py-1 
                    text-sm font-semibold text-gray-700 mr-2 mb-2">Population: {{c.population}}</span>
                    <span class="inline-block bg-gray-200 rounded-full px-3 py-1 
                    text-sm font-semibold text-gray-700 mr-2 mb-2">Region: {{c.region}}</span>
                    <span class="inline-block bg-gray-200 rounded-full px-3 py-1 
                    text-sm font-semibold text-gray-700 mr-2 mb-2">Demonym: {{c.demonym}}</span>
                </div>
                </div>
            </div>
        </div>
    </div>
    <div v-else>
    <div v-if="countries.length > 0" 
            class="p-10 grid grid-cols-1 sm:grid-cols-1 md:grid-cols-3 
            lg:grid-cols-3 xl:grid-cols-4 gap-5">
            <!--Card 1-->
            <div class="rounded overflow-hidden shadow-lg"
            v-for="country in countries" :key="country.title" >
            <img class="w-full" :src="country.flag" alt="Mountain">
            <div class="px-6 py-4">
                <div class="font-bold text-xl mb-2">{{country.name}}</div>
                <p class="text-gray-700 text-base">
            Capital City: {{country.capital}}
                </p>
            </div>
            <div class="px-6 pt-4 pb-2">
                <span class="inline-block bg-gray-200 rounded-full px-3 py-1 
                text-sm font-semibold text-gray-700 mr-2 mb-2">Population: {{country.population}}</span>
                <span class="inline-block bg-gray-200 rounded-full px-3 py-1 
                text-sm font-semibold text-gray-700 mr-2 mb-2">Region: {{country.region}}</span>
                <span class="inline-block bg-gray-200 rounded-full px-3 py-1 
                text-sm font-semibold text-gray-700 mr-2 mb-2">Demonym: {{country.demonym}}</span>
                <button @click.prevent="showCountry(country.alpha2Code)" class="bg-orange-400 py-3 px-8 mt-4 rounded text-sm text-gray-200
                font-semibold hover:bg-orange-700">show countries</button>
            </div>
            </div>
        </div>
    </div>

</div>
  
  
</template>

<script>
import axios from 'axios';


export default {
    name: "listofcountrie",
      data() {
        return {
            title: 'list of countries',
            countries: [],
            country:{},
            show_country:false
        }
    },
    methods:{
      fetchCountries: function (params) {
          let url = 'https://restcountries.com/v2/all';
          axios.get(url).then(res=>{
              this.countries = res.data
              console.log(this.countries);
          })
      },
      showCountry: function (alphaCode) {
         let allCountries = this.countries;
         let country = allCountries.filter(country=>country.alpha2Code == alphaCode);
         this.country = country;
         this.show_country = true;
         console.log(country);
      },
      showCountries: function(){
          this.show_country = false;
      }
    },
    mounted(){
        this.fetchCountries()
    }
}
</script>

<style>

</style>