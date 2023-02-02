<script>

import AppMainActions from './AppMainActions.vue';

export default {
    name: 'AppMain',
    components: {
        AppMainActions 
    }
};

</script>


<template>

    <main>
        
        <!-- Main Content -->
        <section class="mainContentSection">
            <div class="container">

                <span>-- Content goes here --</span>

            </div> <!-- /container-->
        </section> <!-- /mainContentSection-->


        <section class="actionsSection">
            <div class="container">

                <AppMainActions />

            </div> <!-- /container-->
        </section> <!-- /actionsSection-->

    </main>
    
</template>


<style lang="scss" scoped>
    @import "../styles/main.scss";
    @import "../styles/partials/mixin.scss";

    .mainContentSection {
        background-color: $dark-color;
        padding: $spacing-large;

        span {
            font-size: 2rem;
            font-weight: bold;
            color: white;
        }
    }

    .actionsSection {
        background-color: $brand-color;
        padding: $spacing-large;
        
        .container {
            padding: 0 $spacing-large;
        }
    }

</style>