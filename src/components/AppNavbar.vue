<script>

export default {
    name: 'AppNavbar',
    data () {
        return {
            navbar: [
            {
                title: "characters",
                active: false
            },
            {
                title: "comics",
                active: true
            },
            {
                title: "movies",
                active: false
            },
            {
                title: "tv",
                active: false
            },
            {
                title: "games",
                active: false
            },
            {
                title: "collectibles",
                active: false
            },
            {
                title: "videos",
                active: false
            },
            {
                title: "fans",
                active: false
            },
            {
                title: "news",
                active: false
            },
            {
                title: "shop",
                active: false
            },
        ]
        }
    }
}
</script>


<template>
    <nav>

        <ul>

            <li v-for="item in navbar" :class="(item.active) ? ('active') : ('')">
                <a href="#">
                    {{ item.title }}
                </a>
            </li>

        </ul>

    </nav>
</template>


<style lang="scss" scoped>
    @import "../styles/partials/mixin.scss";
    @import "../styles/main.scss";

    nav {
        height: 110px;
        user-select: none;
    }

    ul {
        @include flexRowSpaced;

        list-style: none;
        height: 100%;

        li {
            height: 100%;
            position: relative;
            color: $dark-color;
            transition: color 0.1s;

            &.active {
                
                > a {
                    color: $brand-color;
                }

                &::after {
                position: absolute;
                bottom: 0;
                left: 0;
                background-color: $brand-color;
                
                content: '';
                width: 100%;
                height: 6px;
                }
            }

            &:not(.active):hover {
                color: #757575;
            }

            &:active:not(.active) {
                color: $brand-color !important;
                opacity: 0.6;
            }

            a {
                display: inline-block;
                height: 100%;

                text-decoration: none;
                text-transform: uppercase;
                color: unset;
                font-family: 'Blinker', sans-serif;
                font-size: 0.9rem;
                font-weight: 600;
                line-height: calc(110px - 6px); //Altezza totale - paddingY

                padding: 3px;
            }
        }
    }

</style>