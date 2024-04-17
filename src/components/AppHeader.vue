<script>
export default{
    name: 'AppHeader',
}
</script>

<template>

    <header>
        <div class="big-container my-d-flex">
            <h1>Boolflix</h1>
            <div>
                <input type="text" placeholder="Ricerca il film o serie tv">
                <button>Cerca</button>
            </div>
        </div>
    </header>

</template>

<style scoped lang="scss">
@use '../style/partials/variables' as*;

header{
    background-color: $bg-primary;
    min-height: 70px;
    padding: 10px 0;

    .my-d-flex{
        justify-content: space-between;
        align-items: center;

        h1{
            color: $primary-color;
        }

        input{
            margin-right: 10px;
            width: 200px;
        }
    }

   
}
</style>