<script>
export default{
    name: 'SingleCard',
    props: {
        infoCard: Object
    },
    data(){
        return{
            flagsSup: [
                'it',
                'en',
                'es'
            ]
        }
    },
    methods:{
        getFlagUrl() {
            let flagImage = this.infoCard.original_language + '.png';
	        return new URL(`../assets/img-flags/${flagImage}`, import.meta.url).href   
        }
    }
}
</script>

<template>

    <div class="card">
        <div class="img-space">
            <img v-if="infoCard.poster_path" :src="`https://image.tmdb.org/t/p/w342${infoCard.poster_path}`" alt="">
            <div v-else> Immagine non disponibile</div>
        </div>

        <div class="info-card">
            <!-- titolo -->
            <h4 v-if="infoCard.title">{{ infoCard.title }}</h4>
            <h4 v-else>{{ infoCard.name }}</h4>
            <!-- titolo originale -->
            <h5 v-if="infoCard.original_title">{{ infoCard.original_title }}</h5>
            <h5 v-else>{{ infoCard.original_name }}</h5>
            <!-- lingua e voto -->
            <div>
                <div class="language">
                    {{ infoCard.original_language }}
                    <img v-if="flagsSup.includes(infoCard.original_language)" :src="getFlagUrl()" alt="infoCard.original_language">
                    <span v-else>{{ infoCard.original_language }}</span>
                </div>
                <span>Voto: {{ infoCard.vote_average }}</span>
                
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

        img{
            width: 22px;
        }

        h4{
            margin-bottom: 10px;
        }
    }
}
</style>