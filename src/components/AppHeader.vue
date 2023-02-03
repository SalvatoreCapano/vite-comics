<script>

    import AppNavbar from './AppNavbar.vue';

    export default {
        name: 'AppHeader',
        components: {
            AppNavbar
        }
    }

</script>


<template>
    <header>
        <div class="container">

            <div class="imgContainer">
                <a href="index.html">
                    <img src="../assets/dc-logo.png" alt="Logo DC">
                </a>
            </div> <!-- /imgContainer-->

            <AppNavbar />

        </div> <!-- /container-->
    </header>
</template>


<style lang="scss" scoped>
    @import "../styles/partials/mixin.scss";

    header {
        background-color: #ffffff;

        position: sticky;
        top: 0;
        left: 0;
        z-index: 30;
    }
    .container {
        @include flexSpaceBtwn;
    }
    .imgContainer {
        height: 70px;
        
        a {
            display: inline-block;
            height: 100%;

            img {
                max-height: 100%;
            }
        }
    }

</style>