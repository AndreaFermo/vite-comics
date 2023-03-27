<script>
export default {
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
    <div class="cards">
        <div v-for="section in sections" class="card">
            <h2 class="card-title">{{ section.name }}</h2>
            <ul>
                <li v-for="content in section.contents">
                    <a href="#">{{ content }}</a>
                </li>
            </ul>
        </div>
    </div>
    <div>
        <div>
            <div>SIGN-UP NOW!</div>
            <div>
                <a href="#">FOLLOW US</a>
                <ul>
                    <li v-for="image in imagesName"><img :src="getImagePath(image)" alt=""></li>
                </ul>
            </div>
        </div>
    </div>
</template>
<style scoped></style>