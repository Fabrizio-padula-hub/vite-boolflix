<script>
import axios from 'axios';
import { store } from "./store.js";
import AppHeader from "./components/AppHeader.vue";
import AppMainCard from "./components/AppMainCard.vue";

export default{
  components: {
    AppHeader,
    AppMainCard,
  },
  data(){
    return{
      store
    }
  },
  methods: {
    getElementsFromApi(){
      // stabilire i parametri della chiamata
      const queryParams = {
        api_key: '3a769a04aabe04949f491739be006f35',
        query: store.searchUser
      }

      // fare la chiamata per i film
      axios.get('https://api.themoviedb.org/3/search/movie',{
        params: queryParams 
      })
      .then((response) => {
        store.elementsListMuvies = response.data.results;
      });

      // fare la chiamata per le serie tv
      axios.get('https://api.themoviedb.org/3/search/tv',{
        params: queryParams 
      })
      .then((response) => {
        store.elementsListSeries = response.data.results;
      });
    }
  }
}
</script>

<template>
  <AppHeader @searchText="getElementsFromApi()"></AppHeader>

  <main>
    <AppMainCard></AppMainCard>

  </main>

</template>

<style lang="scss">
@use './style/generic';


</style>
