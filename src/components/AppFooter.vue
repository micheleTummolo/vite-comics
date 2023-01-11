<script>
export default {
    data() {
        return {
            menu: [
                {
                    title: "dc comics",
                    items: [
                        "characters",
                        "comics",
                        "movies",
                        "tv",
                        "games",
                        "videos",
                        "news"
                    ]
                },
                {
                    title: "shop",
                    items: [
                        "shop DC",
                        "shop DC Collectibles"
                    ]
                },
                {
                    title: "dc",
                    items: [
                        "terms of use",
                        "privacy policy (new)",
                        "ad choises",
                        "jobs",
                        "subscriptions",
                        "talent workshops",
                        "CPSC certificates",
                        "ratings",
                        "shop help",
                        "contact us",
                    ]
                },
                {
                    title: "sites",
                    items: [
                        "dc",
                        "mad magazine",
                        "dc kids",
                        "dc universe",
                        "dc power vista",
                    ]
                },
            ],
        }
    }

}
</script>
<template lang="">
    <footer>
        <div class="footer_container">
            <div class="footer_menu_container">
                <div class="menu_container">
                    <nav v-for="(item, index) in menu">
                        <h3>{{item.title}}</h3>
                        <ul>
                            <li v-for="(it, i) in menu[index].items">
                                <a href="">{{it}}</a>
                            </li>
                        </ul>
                    </nav>
                </div>
                <div class="footer_logo">
                </div>
            </div>
        </div>
        <div class="footer_social_container">
            <div>
                <button><a href="#">SIGN-UP NOW!</a></button>
            </div>

            <div class="follow_us">
                <h4>FOLLOW US</h4>
                <div class="social_icon_container">
                    <a href="#">
                        <img src="../assets/images/footer-facebook.png" alt="'footer-facebook.png'">
                    </a>
                    <a href="#">
                        <img src="../assets/images/footer-twitter.png" alt="'footer-twitter.png'">
                    </a>
                    <a href="#">
                        <img src="../assets/images/footer-youtube.png" alt="'footer-youtube.png'">
                    </a>
                    <a href="#">
                        <img src="../assets/images/footer-pinterest.png" alt="'footer-pinterest.png'">
                    </a>
                    <a href="#">
                        <img src="../assets/images/footer-periscope.png" alt="'footer-periscope.png'">
                    </a>
                </div>
            </div>
        </div>
    </footer>
</template>
<style lang="scss">
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

footer {
    background-color: rgb(48, 48, 48);

    .footer_container {
        background-image: url("../assets/images/footer-bg.jpg");
        background-size: cover;

        .footer_menu_container {
            @include main_center;
            @include flex_between;

            .menu_container {
                display: flex;
                flex-direction: column;
                flex-wrap: wrap;
                height: 320px;
                width: 50%;
                padding-top: 3rem;

                nav {
                    margin-bottom: 1rem;

                    h3 {
                        color: $color_white;
                        text-transform: uppercase;
                        margin-bottom: .6rem;
                    }

                    a {
                        text-transform: capitalize;
                        color: rgb(116, 116, 116);
                        font-weight: 300;
                        font-size: .9rem;

                        &:hover {
                            color: $color_white;
                            text-decoration: underline;
                        }
                    }
                }
            }

            .footer_logo {
                width: 45%;
                background-image: url('../assets/images/dc-logo-bg.png');
                background-size: cover;
                background-position: center;
            }
        }
    }

    .footer_social_container {
        @include main_center;
        @include flex_between;
        padding: 1rem 0;

        button {
            @include button_blu;
        }

        .follow_us {
            @include flex_align_center;

            h4 {
                color: $primary_color;
                margin-right: 1rem;
            }

            .social_icon_container {
                display: flex;

                img {
                    margin-left: .7rem;
                    width: 27px;
                    height: 27px;
                    display: block;
                }
            }
        }

    }
}
</style>