<template>
     <footer>
         <div class="container footer">
             <div class="footer__top">
                <div class="top__list">
                    <div class="list__col">
                        <h5>DC COMICS</h5>
                        <ul class="col__list">
                            <li><a href="#">d</a></li>
                        </ul>
                        <h5>SHOP</h5>
                        <ul class="col__list">
                            <li><a href="#">d</a></li>
                        </ul>
                    </div>
                    <div class="list__col">
                        <h5>DC</h5>
                        <ul class="col__list">
                            <li><a href="#">d</a></li>
                        </ul>
                     </div>
                    <div class="list__col">
                        <h5>DC</h5>
                        <ul class="col__list">
                            <li><a href="#">d</a></li>
                        </ul>
                    </div>
                </div>
             </div>
             <div class="footer__bottom"></div>
         </div>
     </footer>
</template>

<script>
export default {
    name: "Footer",
    data() {
        return {
            dcComics: [
                {
                    text:"",
                    url:""
                }
            ],
            shop: [

            ],
            dc: [

            ],
            sites: [

            ],
        }
    }
}
</script>

<style scoped lang="scss">
    @import '@/assets/style/common';
    @import '@/assets/style/variables';

    footer {
        background-color: $grey300;
        .footer {
            &__top {
                a {
                    color: $grey500;
                }

                .top__list{
                    display: flex;
                    justify-content: flex-start;
                }
            }
        }
    }
</style>