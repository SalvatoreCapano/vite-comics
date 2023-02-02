<script>

export default {
    name: 'AppMain',
    data () {
        return {
            actions: [
                {
                    imgUrl: "buy-comics-digital-comics.png",
                    title: "digital comics"
                },
                {
                    imgUrl: "buy-comics-merchandise.png",
                    title: "dc merchandise"
                },
                {
                    imgUrl: "buy-comics-subscriptions.png",
                    title: "subscriptions"
                },
                {
                    imgUrl: "buy-comics-shop-locator.png",
                    title: "comic shop locator"
                },
                {
                    imgUrl: "buy-dc-power-visa.svg",
                    title: "dc power visa"
                },
            ]
        }
    },
    methods: {
        getImagePath: function (imgPath) {
            return new URL(imgPath, import.meta.url).href;
        }
    }
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

                    <li v-for="action in actions">
                        <a href="#">
                            <div class="imgContainer">
                                <img :src="getImagePath(`../assets/${action.imgUrl}`)" :alt="action.title">
                            </div> <!-- /imgContainer-->
                            <span class="textContainer">
                                {{ action.title }}
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