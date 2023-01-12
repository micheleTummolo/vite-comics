<script>
export default {
    data() {
        return {

        }
    }
}
</script>
<template lang="">
    <div class="central_menu_container">
        <div class="menu_list">
            <ul>
                <li>
                    <img src="../assets/images/buy-comics-digital-comics.png" alt="buy-comics.digital-comics.png">
                    <a href="#">DIGITAL COMICS</a>
                </li>
                <li>
                    <img src="../assets/images/buy-comics-merchandise.png" alt="buy-comics.merchandise.png">
                    <a href="#">DC MERCHANDISE</a>
                </li>
                <li>
                    <img src="../assets/images/buy-comics-subscriptions.png" alt="buy-comics.subscriptions.png">
                    <a href="#">SUBSCRIPTION</a>
                </li>
                <li>
                    <img src="../assets/images/buy-comics-shop-locator.png" alt="buy-comics.shop-locator.png">
                    <a href="#">COMIC SHOP LOCATOR</a>
                </li>
                <li>
                    <img id="dc_visa" src="../assets/images/buy-dc-power-visa.svg" alt="buy-comics.shop-locator.svg">
                    <a href="#">DC POWER VISA</a>
                </li>
            </ul>
        </div>
    </div>
</template>
<style lang="scss">
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

.central_menu_container {
    background-color: $primary_color;

    .menu_list {
        @include main_center;
        padding: 2rem 0;

        ul {
            @include flex_between;

            li {
                @include flex_align_center;

                img {
                    height: 39px;
                    margin-right: .7rem;
                }

                #dc_visa {
                    height: 25px;
                }

                a{
                    color: $color_white;
                    font-size: .7rem;

                    &:hover {
                        text-decoration: underline;
                    }
                }
            }
        }
    }
}
    
</style>