<script>

    import AppMainActions from './AppMainActions.vue';
    import SeriesCard from './SeriesCard.vue';
    import seriesData from '../data/dc-comics.json'

    export default {
        name: 'AppMain',
        components: {
            AppMainActions,
            SeriesCard
        },
        data() {
            return {
                seriesData: seriesData,
            };
        },
    };

</script>


<template>

    <main>
        
        <!-- Main Content -->
        <section class="heroSection">
        </section> <!-- /heroSection-->


        <section class="contentSection">

            <div class="container">

                <h2 class="sectionTitle">current series</h2>

                <div class="cardsContainer">

                    <SeriesCard class="card" v-for="elem in seriesData"
                        :title="elem.series"
                        :url="elem.thumb"
                    />

                </div> <!-- /cardsContainer-->

                <button class="actionBtn">load more</button>

            </div> <!-- /container-->

        </section> <!-- /contentSection-->


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

    .heroSection {
        height: 420px;

        background-image: url("../assets/jumbotron.jpg");
        background-size: cover;
        background-position: center top;
    }

    .contentSection {
        background-color: $dark-color;

        .container {
            padding-bottom: 1rem;
        }

        .sectionTitle {
            color: white;

            background-color: $brand-color;
            display: inline-block;
            padding: 10px 20px;

            text-transform: uppercase;
            position: relative;
            top: -25px;
        }

        .cardsContainer {
            padding: 1rem;
            margin-bottom: 1rem;

            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 2rem 1.25rem;

            .card {
                width: 165px;
            }
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