<script>
export default{
    name: 'SingleCard',
}
</script>

<template>

    <div class="card">
        <div class="img-space">
            
        </div>

        <div class="info-card">
            <h4>[Titolo]</h4>
            <h5>[Titolo Originale]</h5>
            <div>
                [Lingua]
                [Voto]
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
        height: 170px;
    }
    .info-card{
        margin-top: 10px;

        h4{
            margin-bottom: 10px;
        }
    }

}


</style>