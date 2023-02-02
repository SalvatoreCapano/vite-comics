<script>

export default {
    name: 'AppNavbar'
}
</script>


<template>
    <nav>

        <ul>
            <li>
                <a href="#">characters</a>
            </li>

            <li class="active">
                <a href="#">comics</a>
            </li>

            <li>
                <a href="#">movies</a>
            </li>

            <li>
                <a href="#">tv</a>
            </li>

            <li>
                <a href="#">games</a>
            </li>

            <li>
                <a href="#">collectibles</a>
            </li>

            <li>
                <a href="#">videos</a>
            </li>

            <li>
                <a href="#">fans</a>
            </li>

            <li>
                <a href="#">news</a>
            </li>

            <li>
                <a href="#">shop</a>
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