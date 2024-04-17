<script>
import SingleCard from "./SingleCard.vue";
export default{
    name: 'AppMainCard',
    components: {
        SingleCard
    }
}
</script>

<template>

    <section class="all-cards">
        <div class="small-container my-d-flex">
            <SingleCard></SingleCard>
            <SingleCard></SingleCard>
            <SingleCard></SingleCard>
            <SingleCard></SingleCard>
            <SingleCard></SingleCard>
            <SingleCard></SingleCard>
            <SingleCard></SingleCard>
            <SingleCard></SingleCard>
            <SingleCard></SingleCard>
        </div>
        

    </section>

</template>

<style scoped lang="scss">
@use '../style/partials/variables' as*;
.all-cards{
    background-color: $bg-secondary;

    .small-container{
        flex-wrap: wrap;
        justify-content: space-between;
        gap: 20px;
    }
}

</style>