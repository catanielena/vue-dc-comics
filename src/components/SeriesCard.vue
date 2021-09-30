<template>
    <li class="series-list__card">
        <div class="card__img">
            <img :src="item.thumb" :alt="item.series">  
        </div>
        <div class="card__title">
            {{item.series}}
        </div>
    </li>
</template>

<script>
export default {
    name: "SeriesCard",
    props: ['item']
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common';

    .series-list__card {
        width: calc(50% / 3 - $smGapX2);

        .card__img {
            overflow: hidden;
            position: relative;

            img {
                @include objFit--C-T;
                position: absolute;
            }

        }

        .card__img::after {
            content: "";
            display: inline-block;
            padding-bottom: 100%;
        }

        .card__title {
            height: 5rem;
            text-transform: uppercase;
            font-weight: 400;
            font-size: 1rem;
            margin-top: $smGapX2;
        }

    }
</style>