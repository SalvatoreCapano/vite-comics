<script>

export default {
    name: 'AppMain',
    // components: {
        
    // }
}
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
                
                <ul>

                    <li>
                        <a href="#">
                            <div class="imgContainer">
                                <img src="../assets/buy-comics-digital-comics.png" alt="Digital Comics">
                            </div> <!-- /imgContainer-->
                            <span class="textContainer">
                                digital comics
                            </span> <!-- /textContainer-->
                        </a>
                    </li>

                    <li>
                        <a href="#">
                            <div class="imgContainer">
                                <img src="../assets/buy-comics-merchandise.png" alt="DC Merchandise">
                            </div> <!-- /imgContainer-->
                            <span class="textContainer">
                                dc merchandise
                            </span> <!-- /textContainer-->
                        </a>
                    </li>

                    <li>
                        <a href="#">
                            <div class="imgContainer">
                                <img src="../assets/buy-comics-subscriptions.png" alt="Subscription">
                            </div> <!-- /imgContainer-->
                            <span class="textContainer">
                                subscription
                            </span> <!-- /textContainer-->
                        </a>
                    </li>

                    <li>
                        <a href="#">
                            <div class="imgContainer">
                                <img src="../assets/buy-comics-shop-locator.png" alt="Comic Shop Locator">
                            </div> <!-- /imgContainer-->
                            <span class="textContainer">
                                comic shop locator
                            </span> <!-- /textContainer-->
                        </a>
                    </li>

                    <li>
                        <a href="#">
                            <div class="imgContainer">
                                <img src="../assets/buy-dc-power-visa.svg" alt="DC Power Visa">
                            </div> <!-- /imgContainer-->
                            <span class="textContainer">
                                dc power visa
                            </span> <!-- /textContainer-->
                        </a>
                    </li>

                </ul>

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

        ul {
            @include flexRowSpaced;
            gap: 3rem;
            list-style: none;

            li a {
                @include flexRowSpaced;
                gap: 0.4rem;
                text-decoration: none;
                white-space: nowrap;

                .imgContainer {
                    height: 60px;
                    width: 60px;

                    img {
                        max-width: 100%;
                        max-height: 100%;
                    }
                }

                .textContainer {
                    color: #ffffff;
                    text-transform: uppercase;
                    font-size: 0.8rem;
                    font-weight: 600;
                }

                &:hover {
                    filter: contrast(40%);
                }
            }
        }
    }

</style>