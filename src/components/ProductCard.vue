<template>
    <div class="card">
        <div class="image-wrapper">
            <img :src="image" :alt="title">
        </div>
        <h5>{{ title }}</h5>
    </div>
</template>
<script>

export default {
    name: 'ProductCard',
    props: {
        image: String,
        title: String,
    }
}
</script>
<style scoped lang="scss">
.card {
    margin: 10px;
    width: calc((100% / 6) - 20px);

    .image-wrapper {
        aspect-ratio: 1;
        overflow: hidden;

        img {
            width: 100%;
            object-fit: cover;
            overflow: hidden;
        }
    }

    h5 {
        margin: 10px 0px;
    }


}
</style>