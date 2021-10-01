<template>
    <div class="jumbotron">
        <img :src="heroImg" :alt="heroCaption">
    </div>    
</template>

<script>
export default {
    name: "Hero",
    props: {
        heroImg: String,
        heroCaption: String
    }
}
</script>

<style lang="scss">
@import '../assets/style/common';

    .jumbotron {
        height: 25rem;
        overflow: hidden;
        img {
            @include objFit--C-T;
        }
    }
</style>