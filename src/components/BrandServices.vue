<template>
    <section class="BrandServices">     
        <div class="container services">
            <ul class="services__list">
                <li class="list__item" v-for="(service, i) in serviceList" :key="`service${i}`">
                    <div class="item__img">
                        <img :src="require(`@/assets/img/${service.img}`)" :alt="service.text">
                    </div>
                    <a :href="service.url">{{service.text}}</a>
                </li>
            </ul>
        </div>
    </section>
</template>

<script>
export default {
    name: "BrandServices",
    data() {
        return {
            serviceList: [
                {
                    text: "digital comics",
                    img: "buy-comics-digital-comics.png",
                    url:"#"
                },
                {
                    text: "dc merchandise",
                    img: "buy-comics-merchandise.png",
                    url:"#"
                },
                {
                    text: "subscription",
                    img: "buy-comics-subscriptions.png",
                    url:"#"
                },
                {
                    text: "comic shop locator",
                    img: "buy-comics-shop-locator.png",
                    url:"#"
                },
                {
                    text: "dc power visa",
                    img: "buy-dc-power-visa.svg",
                    url:"#"
                },
                
            ]
        }
    }
}
</script>

<style scoped lang="scss">
    @import '@/assets/style/common';
    @import '@/assets/style/variables';
    
    .BrandServices {
        background-color: $mainColor;
        padding: $sectionPadding;
        .services {

            &__list {
                @include flex--SB-C;
                .list__item {
                    display: flex;
                    align-items: center;

                    .item__img {
                        height: 3.125rem;
                        img {
                            max-width: 3.125rem;
                            height: 100%;
                        }
                    }
                    a {
                        color: #fff;
                        margin: 0 .9375rem;
                    }
                }
            }
        }
    }
</style>