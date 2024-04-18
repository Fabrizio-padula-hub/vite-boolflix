<script>
export default{
    name: 'SingleCard',
    props: {
        infoCard: Object
    }
}
</script>

<template>

    <div class="card">
        <div class="img-space">
            <img src="https://image.tmdb.org/t/p/w500/cNYYPcbcfT90wTyI6hUmJH5Fx8H.jpg" alt="">
        </div>

        <div class="info-card">
            <h4>{{ infoCard.title }}</h4>
            <h5>{{ infoCard.original_title }}</h5>
            <div>
                {{ infoCard.original_language }}
                {{ infoCard.vote_average }}
            </div>
        </div>
    </div>

</template>

<style scoped lang="scss">
@use '../style/partials/variables' as*;
.card{
    color: white;
    width: calc(100% / 6 - 20px);
    margin: 36px 0;

    .img-space{
        border: 1px solid white;
        height: 210px;

        img{
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
    }
    .info-card{
        margin-top: 10px;

        h4{
            margin-bottom: 10px;
        }
    }

}


</style>