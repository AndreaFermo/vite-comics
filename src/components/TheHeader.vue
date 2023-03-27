<script>
export default {
    data() {
        return {
            imageName: 'dc-logo.png',
            sections: ['CHARACTERS', 'COMICS', 'MOVIES', 'TV', 'GAMES', 'COLLEVCTIBLES', 'VIDEOS', 'FANS', 'NEWS', 'SHOP']
        };
    },
    methods: {
        getImagePath: function (img) {
            return new URL(`../assets/${img}`, import.meta.url).href;
        }
    }
};

</script>

<template>
    <nav>
        <img :src="getImagePath(imageName)" alt="">
        <ul class="nav-bar">
            <li v-for="section in sections"><a href="#">{{ section }}</a></li>
        </ul>
    </nav>
</template>

<style scoped lang="scss">
@use "../styles/partials/mixins";

nav {
    @include mixins.d-flex-center;
}

.nav-bar {
    display: flex;
    list-style: none;
}
</style>
