<script>
import AppHeader from "./components/AppHeader.vue";
import AppMainCard from "./components/AppMainCard.vue";

export default{
  components: {
    AppHeader,
    AppMainCard,
  }
}
</script>

<template>
  <AppHeader></AppHeader>

  <main>
    <AppMainCard></AppMainCard>

  </main>

</template>

<style lang="scss">
@use './style/generic';


</style>
