<template>
    <div class="cards">
        <ProductCard v-for="(comic, index) in comicsList" :key="index" :image="comic.thumb" :title="comic.series">
        </ProductCard>
    </div>
    <div class="button-container">
        <a href="#">LOAD MORE</a>
    </div>
</template>
<script>
import ProductCard from './ProductCard.vue';
export default {
    name: 'ProductsList',
    components: {
        ProductCard,
    },
    props: {
        comicsList: Array,
    }
}
</script>
<style scoped lang="scss">
@use "../styles/partials/variables";

.cards {
    display: flex;
    flex-wrap: wrap;
    padding: 30px 0px;
}

.button-container {
    display: flex;

    a {
        background-color: variables.$color-secondary;
        text-decoration: none;
        padding: 5px 30px;
        color: variables.$color-white;
        font-weight: bold;
        margin: 15px auto;

    }
}
</style>