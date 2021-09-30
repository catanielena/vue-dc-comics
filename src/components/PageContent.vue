<template>
    <section class="PageContent">   
        <!-- jumbotron -->
        <div class="PageContent__jumbotron">
            <img src="../assets/img/jumbotron.jpg" alt="jumbotron-img">
        </div>  
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

export default {
    name: "PageContent",
    components: { SeriesCard },
    data() {
        return {
            currentSeries: []
        }
    },
    mounted() {
        fetch('../assets/data/dc-comics.json')
        .then(response => this.currentSeries = response.data)
    }
}
</script>

<style scoped lang="scss">
    @import '../assets/style/common';

    .PageContent {
        background-color: $grey100;
        font-weight: 700;
        $this: &;

        &__jumbotron {
            height: 25rem;
            overflow: hidden;
            img {
                @include objFit--C-T;
            }
        }

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