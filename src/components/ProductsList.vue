<template>
    <div class="cards">
        <ProductCard v-for="(comic, index) in comicsList" :key="index" :image="comic.thumb" :title="comic.series">
        </ProductCard>
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
.cards {
    display: flex;
    flex-wrap: wrap;
    padding: 30px 0px;
}
</style>