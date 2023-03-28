<template>
    <div class="bonus-container">
        <div class="cards">
            <div v-for="(element, index) in bonus" :key="index" class="card">
                <img :src="getImagePath(element.image)" :alt="element.text">
                <span>{{ element.text }}</span>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name: 'TheBonus',
    data() {
        return {
            bonus: [
                {
                    image: 'buy-comics-digital-comics.png',
                    text: 'DIGITAL COMICS'
                },
                {
                    image: 'buy-comics-merchandise.png',
                    text: 'DC MERCHANDISE'
                },
                {
                    image: 'buy-comics-subscriptions.png',
                    text: 'SUBSCRIPTION'
                },
                {
                    image: 'buy-comics-shop-locator.png',
                    text: 'COMIC SHOP LOCATOR'
                },
                {
                    image: 'buy-dc-power-visa.svg',
                    text: 'DC POWER VISA'
                }
            ]
        }
    },
    methods: {
        getImagePath: function (img) {
            return new URL(`../assets/${img}`, import.meta.url).href;
        }
    }
}
</script>
<style scoped lang="scss">
@use "../styles/partials/variables";

.bonus-container {
    background-color: variables.$color-secondary;
    height: 150px;
}

.cards {
    line-height: 150px;
    width: 1100px;
    margin: auto;
    display: flex;
    justify-content: space-around;

    .card {
        display: flex;
        align-items: center;

        &:last-child img {
            height: 30px;
        }

        img {
            height: 50px;
            margin-right: 15px;
        }

        span {
            font-size: 10px;
        }
    }
}
</style>