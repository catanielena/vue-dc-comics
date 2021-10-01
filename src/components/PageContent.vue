<template>
    <section class="PageContent">   
        <!-- jumbotron -->
        <Hero :heroImg="require('../assets/img/jumbotron.jpg')" :heroCaption="'cartoon_bg'"/>
        <!-- /jumbotron -->
        <!-- current series -->
        <div class="container PageContent__sct-series">
            <h3 class="sct-series__title">Current series</h3>
            <ul class="sct-series__series-list">
                <SeriesCard v-for="(item, i) in currentSeries" :key="i" :item="item"/>
            </ul>
            <div class="sct-series__btn">
                <button class="btn">LOAD MORE</button>
            </div>
        </div>
        <!-- /current series -->
    </section>
</template>

<script>
import SeriesCard from '../components/SeriesCard.vue';
import Hero from '../components/Hero.vue';

import axios from "axios";
export default {
    name: "PageContent",
    components: { SeriesCard, Hero },
    data() {
        return {
            currentSeries: []
        }
    },
    mounted() {
        // axios.get('../data/dc-comics.json')
        // .then(response =>this.currentSeries = response.data)
        // .catch((err) => console.log(err))
        axios
            .get('../data/dc-comics.json')
            .then(response => (this.currentSeries = response.data))
            .catch(error => console.log(error))
    }
}
</script>

<style scoped lang="scss">
    @import '../assets/style/common';

    .PageContent {
        background-color: $grey100;
        font-weight: 700;
        $this: &;

        &__sct-series {
            .sct-series__series-list {
                @include flex--SB-C;
                @include inlineList;
                flex-wrap: wrap;
            }

            .sct-series__title {
                position: relative;
                display: inline-block;
                padding: .8rem 2rem;
                transform: translateY(-50%);
                background-color: $mainColor;
            }

            .sct-series__btn {
                text-align: center;
            }

            .btn {
                margin: $smGapX2;
                background-color: $mainColor;
                padding: .8rem 4.375rem;
                font-weight: 700;
            }
        }

    }
</style>