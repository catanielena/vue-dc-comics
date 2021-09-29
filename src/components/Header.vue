<template>
    <header>
        <div class="container header">
            <div class="header__logo">
                <img class="logo__img" src="@/assets/img/dc-logo.png" alt="dc-logo">
            </div>
            <nav class="header__nav">
                <ul class="nav__list">
                    <li class="list__item" v-for="(link, i) in nav" :key="`header__listItem${i}`"><a :class="{active: link.current}" href="#">{{link.text}}</a></li>            
                </ul>
            </nav>
        </div>
    </header>  
</template>

<script>
export default {
    name: "Header",
    data() {
        return {
            nav: [
                {
                    text: "characters",
                    url: "#",
                    current: false
                },
                {
                    text: "comics",
                    url: "#",
                    current: true
                },
                                {
                    text: "movies",
                    url: "#",
                    current: false
                },
                {
                    text: "tv",
                    url: "#",
                    current: false
                },
                                {
                    text: "games",
                    url: "#",
                    current: false
                },
                {
                    text: "collectibles",
                    url: "#",
                    current: false
                },
                                {
                    text: "videos",
                    url: "#",
                    current: false
                },
                {
                    text: "fans",
                    url: "#",
                    current: false
                },
                                {
                    text: "news",
                    url: "#",
                    current: false
                },
                {
                    text: "shop",
                    url: "#",
                    current: false
                }                
            ]
        }

    }
}
</script>

<style scoped lang="scss">
    @import '@/assets/style/common';
    @import '@/assets/style/variables';

    header {
        background-color: #fff;
        position: fixed;
        width: 100%;

        .header {
            display: flex;
            justify-content: space-between;
            align-items: center;

            &__logo {
                height: 4.375rem;

                img{
                    height: 100%
                }
            };
            &__nav {
                ul {
                    display: flex;

                    .list__item {
                        a {
                            line-height: $lineheightLink;
                            margin: 0 1.25rem;
                            font-weight: 700;
                            color: $grey100;
    
                            &.active {
                                border-bottom: 3px solid;
                                color: $mainColor;
                                border-color: $mainColor;
                            }
                        }
                    }
                }
            }
        }

    }
</style>