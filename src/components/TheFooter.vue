<script>
export default {
    name: 'TheFooter',
    data() {
        return {
            sections: [
                {
                    name: 'DC COMICS',
                    contents: ['Characters', 'Comics', 'Movies', 'Tv', 'Games', 'Videos', 'News'],
                },

                {
                    name: 'SHOP',
                    contents: ['Shop DC', 'Shop DC Collectibles'],
                },

                {
                    name: 'DC',
                    contents: ['Terms Of Use', 'Privacy policy (New)', 'Ad Choices', 'Advertising', 'Jobs', 'Subscriptions', 'Talent Workshops', 'CPSC Certificates', 'Ratings', 'Shop Help', 'Contact Us'],
                },

                {
                    name: 'SITES',
                    contents: ['DC', 'MAD Magazine', 'DC Kids', 'DC Universe', 'DC Power Visa'],
                },
            ],
            imagesName: ['facebook', 'twitter', 'youtube', 'pinterest', 'periscope']
        };
    },
    methods: {
        getImagePath: function (img) {
            return new URL(`../assets/footer-${img}.png`, import.meta.url).href;
        }
    }
};
</script>

<template>
    <div class="footer-top">
        <div class="image-wrapper"></div>
        <div class="cards">
            <div v-for="(section, index) in sections" class="card" :key="index">
                <h3 class="card-title">{{ section.name }}</h3>
                <ul>
                    <li v-for="(content, index) in section.contents" :key="index">
                        <a href="#">{{ content }}</a>
                    </li>
                </ul>
            </div>
        </div>
    </div>

    <div class="footer-bottom">
        <div class="footer-wrapper">
            <div class="sign-up-button">SIGN-UP NOW!</div>
            <div class="socials">
                <a href="#">FOLLOW US</a>
                <ul>
                    <li v-for="image in imagesName"><img :src="getImagePath(image)" alt=""></li>
                </ul>
            </div>
        </div>
    </div>
</template>
<style scoped lang="scss">
@use "../styles/partials/mixins";
@use "../styles/partials/variables";

.cards {
    padding: 15px 0px 20px;
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
    height: 380px;
    width: 450px;

    .card {
        width: 150px;
    }

    h3 {
        color: variables.$color-white;
        margin: 15px 0px 20px;
    }

    ul {
        list-style: none;

        li {
            padding: 3px 0px;

            a {
                text-decoration: none;
                color: variables.$color-grey;
                font-size: 12px;
            }
        }
    }
}

.footer-top {
    @include mixins.container;
    height: 380px;
    position: relative;

    .image-wrapper {
        position: absolute;
        top: 0px;
        right: 0px;
        height: 380px;
        width: 600px;
        background-image: url(../assets/dc-logo-bg.png);
        background-repeat: no-repeat;
        background-position: center;

    }
}

.footer-bottom {
    background-color: #303030;

    .footer-wrapper {
        display: flex;
        justify-content: space-between;
        align-items: center;
        @include mixins.container;
        height: 100px;

        .sign-up-button {
            color: variables.$color-white;
            border: 3px solid variables.$color-secondary;
            padding: 12px;

        }

        .socials {
            display: flex;
            align-items: center;

            a {
                text-decoration: none;
                font-size: 20px;
                font-weight: bold;
                color: variables.$color-secondary;
            }

            ul {
                display: flex;
                list-style: none;
                margin-left: 30px;

                li {
                    padding: 10px;
                }
            }
        }
    }

}
</style>