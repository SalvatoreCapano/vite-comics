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
        height: fit-content;
        height: 110px
    }
    
    .container {
        @include flexSpaceBtwn;
    }
    
    .imgContainer {
        height: 100%;
        padding: 0.75rem 0;

        a {
            display: inline-block;
            height: 100%;
        }
    }

</style>