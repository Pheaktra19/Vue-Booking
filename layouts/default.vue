<template>
    <div>
        <SearchBar ></SearchBar>
        <Nuxt id="wrapper" />
        <TheFooter></TheFooter>

    </div>
</template>

<script>
import SearchBar from '~/components/SearchBar.vue';
import TheFooter from '~/components/TheFooter.vue';
    export default {
    components: { SearchBar, TheFooter }
}
</script>

<style scoped>
#wrapper {
    min-height: 100vh;
    
}
</style>