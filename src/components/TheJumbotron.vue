<template>
    <div class="jumbotron-wrapper">
        <div class="button-current-series">CURRENT SERIES</div>
    </div>
</template>

<script>
export default {
    name: 'TheJumbotron',
}
</script>

<style scoped lang="scss">
@use "../styles/partials/variables";

.jumbotron-wrapper {
    height: 400px;
    position: relative;
    background-image: url(../assets/jumbotron.jpg);

    .button-current-series {
        position: absolute;
        bottom: -19px;
        left: 400px;
        background-color: variables.$color-secondary;
        padding: 10px 15px;
        font-weight: bold;
    }


}
</style>


