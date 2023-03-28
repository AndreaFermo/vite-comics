<script>
export default {
    name: 'TheHeader',
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
            <li v-for="(section, index) in sections" :key="index"><a href="#">{{ section }}</a></li>
        </ul>
    </nav>
</template>
<style scoped lang="scss">
@use "../styles/partials/mixins";
@use "../styles/partials/variables";

nav {
    @include mixins.d-flex-between;
    height: 100px;
}

.nav-bar {
    display: flex;
    list-style: none;

    li {
        border-bottom: 3px solid white;
        padding: 0px 5px;

        &:hover {
            border-bottom: 3px solid variables.$color-secondary;

            a {
                color: variables.$color-secondary;
            }
        }
    }

    a {
        color: variables.$color-primary;
        text-decoration: none;
        line-height: 97px;
        font-weight: bold;
        font-size: 14px;
    }
}

img {
    height: 80px;
}
</style>
