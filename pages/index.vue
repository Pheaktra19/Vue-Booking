<template>
  <div>
    <!-- <SearchBar/> -->
    <Search/>
    <Banner/>
    <Explore/>
    <MostPopular/>
    <Footer/>
  </div>
</template>

<script>
import Banner from '~/components/Banner.vue';
import Explore from '~/components/Explore.vue';
import MostPopular from '~/components/MostPopular.vue';
import Search from '~/components/Search.vue';
  export default {
    components: { Banner, Explore, MostPopular, Search }
}
</script>

<style  scoped>

</style>
