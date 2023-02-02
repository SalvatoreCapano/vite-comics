<script>

export default {
    name: 'AppFooter',
    data() {
        return {
            footerLists: [
                {
                    title: "dc comics",
                    elements: ["characters", "comics", "movies", "TV", "games", "videos", "news"]
                },
                {
                    title: "shop",
                    elements: ["shop DC", "shop DC collectibles"]
                },
                {
                    title: "DC",
                    elements: ["terms of use", "privacy policy (new)", "ad choices", "advertising", "jobs", "subscriptions", "talent workshops", "cpsc certificates", "ratings", "shop helperNameMap", "contact us"]
                },
                {
                    title: "sites",
                    elements: ["DC", "MAD magazines", "DC kids", "DC universe", "DC power visa"]
                }
            ],
            socialLinks: [
                {
                    name: "Facebook",
                    imgUrl: "footer-facebook.png"
                },
                {
                    name: "Twitter",
                    imgUrl: "footer-twitter.png"
                },
                {
                    name: "Youtube",
                    imgUrl: "footer-youtube.png"
                },
                {
                    name: "Pinterest",
                    imgUrl: "footer-pinterest.png"
                },
                {
                    name: "Periscope",
                    imgUrl: "footer-periscope.png"
                }
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

    <footer>

        <section class="footerNav">
            <div class="container">

                <div class="textContainer">

                    <div class="col" v-for="list in footerLists">

                        <h3 class="footerListTitle">{{ list.title }}</h3>
                        
                        <ul class="footerList">
                            <li v-for="element in list.elements">
                                <a href="#">{{ element }}</a>
                            </li>
                        </ul>
                         <!-- /footerList-->

                    </div> <!-- /col-->

                </div> <!-- /textContainer-->

                <div class="imgContainer">
                    <img src="../assets/dc-logo-bg.png" alt="DC">
                </div> <!-- /imgContainer-->

            </div> <!-- /container-->
        </section>

        <section class="footerSocial">
            <div class="container">

                <button class="ctaBtn">
                    sign-up now!
                </button>

                <div class="socials">
                    <h3 class="ctaText">follow us</h3>

                    <div>
                        <ul class="socialList">
                            <li v-for="social in socialLinks">
                                <a href="#">
                                    <img :src="getImagePath(`../assets/${social.imgUrl}`)" :alt="social.name">
                                </a>
                            </li>
                        </ul>
                    </div>
                </div>

            </div> <!-- /container-->
        </section>

    </footer>
    
</template>


<style lang="scss" scoped>
    @import "../styles/main.scss";
    @import "../styles/partials/mixin.scss";

    .footerNav {
        padding: $spacing-large 0;

        background-image: url("../assets/footer-bg.jpg");
        background-repeat: no-repeat;
        background-size: cover;
        overflow: hidden;

        height: 450px;

        .container {
            @include flexSpaceBtwn;
            height: 100%;

            position: relative;
        }

        .textContainer {
            display: flex;
            flex-direction: column;
            flex-wrap: wrap;
            gap: 1.5rem 2.5rem;

            height: 100%;

            .footerListTitle {
                color: #dddddd;
                text-transform: uppercase;
                font-size: 1rem;
                margin-bottom: 1rem;
            }

            .footerList {
                list-style: none;

                a {
                    color: #808080;
                    text-decoration: none;
                    text-transform: capitalize;
                    font-size: 0.8rem;
                    font-weight: 600;

                    &:hover {
                        color: rgb(210, 210, 210);
                    }
                }
            }
        }

        .imgContainer {
            position: absolute;
            right: 0;
            top: 50%;
            transform: translateY(-50%);
        }
    }

    .footerSocial {
        background-color: $less-dark-color;
        padding: $spacing-large 0;

        .container {
            @include flexSpaceBtwn;

            .ctaBtn {
                display: inline-block;
                padding: 16px;

                border: 3px solid $brand-color;
                background-color: $less-dark-color;

                color: #ffffff;
                text-transform: uppercase;
                font-weight: 600;
                font-size: 1.05rem;

                position: relative;
                isolation: isolate;

                cursor: pointer;

                &::after {
                    content: '';
                    position: absolute;
                    bottom: 0;
                    left: 0;
                    z-index: -1;

                    transition: height 0.2s;
                    background-color: $brand-color;
                    opacity: 0.5;

                    width: 100%;
                    height: 0;
                }

                &:hover::after {
                    height: 100%;
                }
            }

            .socials {
                @include flexRowSpaced;

                h3 {
                    color: $brand-color;
                    text-transform: uppercase;
                    font-size: 1.2rem;
                }

                .socialList {
                    @include flexRowSpaced;
                    list-style: none;

                    li:hover {
                        filter: brightness(0) contrast(100%) invert(75%);
                    }
                }
            }
        }
    }

</style>