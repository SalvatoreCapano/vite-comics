<script>

export default {
    name: 'AppFooter',
    // components: {
        
    // }
}
</script>


<template>

    <footer>

        <section class="footerNav">
            <div class="container">

                <div class="textContainer">
                    <div class="col">
                        <div>
                            <h3 class="footerListTitle">dc comics</h3>
                            <ul class="footerList">
                                <li>
                                    <a href="#">character</a>
                                </li>
                                <li>
                                    <a href="#">comics</a>
                                </li>
                                <li>
                                    <a href="#">movies</a>
                                </li>
                                <li>
                                    <a href="#">TV</a>
                                </li>
                                <li>
                                    <a href="#">games</a>
                                </li>
                                <li>
                                    <a href="#">videos</a>
                                </li>
                                <li>
                                    <a href="#">news</a>
                                </li>
                            </ul>
                        </div>

                        <div>
                            <h3 class="footerListTitle">shop</h3>
                            <ul class="footerList">
                                <li>
                                    <a href="#">shop DC</a>
                                </li>
                                <li>
                                    <a href="#">shop DC collectibles</a>
                                </li>
                            </ul>
                        </div>
                    </div> <!-- /col-->

                    <div class="col">
                        <h3 class="footerListTitle">dc</h3>
                            <ul class="footerList">
                                <li>
                                    <a href="#">terms of use</a>
                                </li>
                                <li>
                                    <a href="#">privacy polici (new)</a>
                                </li>
                                <li>
                                    <a href="#">ad choices</a>
                                </li>
                                <li>
                                    <a href="#">advertising</a>
                                </li>
                                <li>
                                    <a href="#">jobs</a>
                                </li>
                                <li>
                                    <a href="#">subscriptions</a>
                                </li>
                                <li>
                                    <a href="#">talent workshops</a>
                                </li>
                                <li>
                                    <a href="#">cpsc certificates</a>
                                </li>
                                <li>
                                    <a href="#">ratings</a>
                                </li>
                                <li>
                                    <a href="#">show help</a>
                                </li>
                                <li>
                                    <a href="#">contact us</a>
                                </li>
                            </ul>
                    </div> <!-- /col-->

                    <div class="col">
                        <h3 class="footerListTitle">sites</h3>
                            <ul class="footerList">
                                <li>
                                    <a href="#">DC</a>
                                </li>
                                <li>
                                    <a href="#">MAD magazines</a>
                                </li>
                                <li>
                                    <a href="#">DC kids</a>
                                </li>
                                <li>
                                    <a href="#">DC universe</a>
                                </li>
                                <li>
                                    <a href="#">DC power visa</a>
                                </li>
                            </ul>
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
                            <li>
                                <a href="#">
                                    <img src="../assets/footer-facebook.png" alt="Facebook">
                                </a>
                            </li>

                            <li>
                                <a href="#">
                                    <img src="../assets/footer-twitter.png" alt="Twitter">
                                </a>
                            </li>

                            <li>
                                <a href="#">
                                    <img src="../assets/footer-youtube.png" alt="Youtube">
                                </a>
                            </li>

                            <li>
                                <a href="#">
                                    <img src="../assets/footer-pinterest.png" alt="Pinterest">
                                </a>
                            </li>

                            <li>
                                <a href="#">
                                    <img src="../assets/footer-periscope.png" alt="Periscope">
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

        .container {
            @include flexSpaceBtwn;

            position: relative;
        }

        .textContainer {
            @include flexRowSpaced;
            align-items: flex-start;
            gap: 2rem;

            .col:first-child > div:first-child {
                margin-bottom: 1.25rem;
            }

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