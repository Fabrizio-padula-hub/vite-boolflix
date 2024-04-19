<script>
import { store } from "../store.js";
import SingleCard from "./SingleCard.vue";
export default{
    name: 'AppMainCard',
    components: {
        SingleCard
    },
    data(){
        return{
            store
        }
    }
}
</script>

<template>

    <section class="all-cards">
        <div class="small-container">
            <h2>Film</h2>
        </div>
        
        <div class="small-container my-d-flex">
            <SingleCard v-for="movies in store.elementsListMuvies" :key="movies.id" :infoCard="movies"></SingleCard>
        </div>

        <div class="small-container">
            <h2>Serie Tv</h2>
        </div>

        <div class="small-container my-d-flex">
            <SingleCard v-for="series in store.elementsListSeries" :key="series.id" :infoCard="series"></SingleCard>
        </div>
        

    </section>

</template>

<style scoped lang="scss">
@use '../style/partials/variables' as*;
.all-cards{
    background-color: $bg-secondary;

    h2{
        color: white;
    }

    .small-container{
        flex-wrap: wrap;
        gap: 20px;
    }
}

</style>