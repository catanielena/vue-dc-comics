<template>
     <footer>
             <div class="footer__top">
                 <div class="container">
                    <div class="top__list">
                        <div class="list__col">
                            <h5>DC COMICS</h5>
                            <ul class="col__list">
                                <li v-for="(item, i) in dcComics" :key="`dcComics_${i}`"><a :href="item.url">{{item.text}}</a></li>
                            </ul>
                            <h5>SHOP</h5>
                            <ul class="col__list">
                                <li v-for="(item, i) in shop" :key="`shop_${i}`"><a :href="item.url">{{item.text}}</a></li>
                            </ul>
                        </div>
                        <div class="list__col">
                            <h5>DC</h5>
                            <ul class="col__list">
                                <li v-for="(item, i) in dc" :key="`dc_${i}`"><a :href="item.url">{{item.text}}</a></li>
                            </ul>
                        </div>
                        <div class="list__col">
                            <h5>SITES</h5>
                            <ul class="col__list">
                                <li v-for="(item, i) in sites" :key="`sites_${i}`"><a :href="item.url">{{item.text}}</a></li>
                            </ul>
                        </div>
                    </div>
                 <div class="top__img">
                     <img src="@/assets/img/dc-logo-bg.png" alt="">
                 </div>
                 </div>
             </div>
             <div class="footer__bottom container">
                <div class="bottom__left">
                    <button type="button" class="btn">SIGN-UP NOW!</button>
                </div>
                <div class="bottom__right">
                    <h4>FOLLOW US</h4>
                    <ul class="right__list">
                        <li class="list__item">
                            <a href="#">
                                <img src="@/assets/img/footer-facebook.png" alt="facebook-icon">
                            </a>
                        </li>
                            <li>
                            <a href="#">
                                <img src="@/assets/img/footer-twitter.png" alt="twitter-icon">
                            </a>
                        </li>
                            <li>
                            <a href="#">
                                <img src="@/assets/img/footer-youtube.png" alt="youtube-icon">
                            </a>
                        </li>
                            <li>
                            <a href="#">
                                <img src="@/assets/img/footer-pinterest.png" alt="pinterest-icon">
                            </a>
                        </li>
                            <li>
                            <a href="#">
                                <img src="@/assets/img/footer-periscope.png" alt="periscope-icon">
                            </a>
                        </li>
                    </ul>
                </div>

             </div>
         
     </footer>
</template>

<script>
export default {
    name: "Footer",
    data() {
        return {
            dcComics: [
                {text:"Characters", url:"#"},
                {text:"Comics", url:"#"},
                {text:"Movies", url:"#"},
                {text:"TV", url:"#"},
                {text:"Games", url:"#"},
                {text:"Videos", url:"#"},
                {text:"News", url:"#"},
            ],
            shop: [
                {text:"Shop DC", url:"#"},
                {text:"Shop DC Collwctiibles", url:"#"}
            ],
            dc: [
                {text:"Terms of Use", url:"#"},
                {text:"Privacy policy (New)", url:"#"},
                {text:"Ad Choices", url:"#"},
                {text:"Advertising", url:"#"},
                {text:"Jobs", url:"#"},
                {text:"Subscription", url:"#"},
                {text:"Talent Workshop", url:"#"},
                {text:"CPSC Certificates", url:"#"},
                {text:"Ratings", url:"#"},
                {text:"Shop Help", url:"#"},
                {text:"Contact Us", url:"#"}
            ],
            sites: [
                {text:"DC", url:"#"},
                {text:"MAD Magazines", url:"#"},
                {text:"DC Kids", url:"#"},
                {text:"DC Universe", url:"#"},
                {text:"DC Power Visa", url:"#"}
            ],
        }
    }
}
</script>

<style scoped lang="scss">
    @import '@/assets/style/common';
    @import '@/assets/style/variables';
    @import '@/assets/style/mixin';
    footer {
        background-color: $grey300;
        .footer {
            $this: &;
            &__top {
                @include bgImg('../assets/img/footer-bg.jpg');
                .container {
                    @include flex--SB-C;
                    overflow: hidden;
                    max-height: 23rem;
                }
                a {
                    color: $grey500;
                    text-transform: inherit;
                }

                .top__list{
                    @include inlineList;
                    justify-content: flex-start;
                }

                .list__col {
                    margin-right: 1.6875rem;
                }

                .col__list {
                    margin: 1.25rem 0;
                }
            }

            &__bottom {
                @include flex--SB-C;
                padding: $sectionPadding;
                .right__list {
                    display: flex;

                    a {
                        width: 2rem;
                        margin: 0 .625rem;
                        img {
                            width: 100%;
                        }
                    }
                }

                .btn {
                    border: 2px solid $mainColor;
                    padding: 1rem;
                    font-size: 1rem;
                }

                .bottom__right {
                    display: flex;
                    align-items: center;

                    h4 {        
                        margin: 0 .625rem;
                        color: $mainColor;
                    }
                }
            }
        }
    }
</style>