<script>
import MainCategories from './main_components/MainCategories.vue';
import MainSeriesCards from './main_components/MainSeriesCards.vue';

export default {
    components: { MainCategories, MainSeriesCards }
}
</script>

<template>
    <main>
        <MainSeriesCards />

        <MainCategories />
    </main>
</template>

<style lang="scss" scoped>

</style>