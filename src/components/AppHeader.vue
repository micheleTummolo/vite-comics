<script>
export default {
    data() {
        return {
            menu: [
                {
                    label: 'characters',
                    url: '#',
                    active: false
                },
                {
                    label: 'comics',
                    url: '#',
                    active: true
                },
                {
                    label: 'movies',
                    url: '#',
                    active: false
                },
                {
                    label: 'tv',
                    url: '#',
                    active: false
                },
                {
                    label: 'games',
                    url: '#',
                    active: false
                },
                {
                    label: 'collectibles',
                    url: '#',
                    active: false
                },
                {
                    label: 'videos',
                    url: '#',
                    active: false
                },
                {
                    label: 'fans',
                    url: '#',
                    active: false
                },
                {
                    label: 'news',
                    url: '#',
                    active: false
                },
                {
                    label: 'shop',
                    url: '#',
                    active: false
                },
            ]
        }
    }

}
</script>
<template lang="">
    <header>
        <div class="header_container">
            <div class="logo_container">
                <img src="../../src/assets/images/dc-logo.png" alt="">
            </div>
    
            <nav>
                <ul>
                    <li v-for="(item, index) in menu">
                        <a :href="item.url" :class="item.active ? 'active' : ''">{{item.label}}</a>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
    <div class="jumbotron">
        <img src="../assets/images/jumbotron.jpg" alt="">
    </div>
</template>
<style lang="scss">
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

header {
    background-color: $color_white;


    .header_container {
        @include main_center;
        @include flex_between;

        .logo_container {
            @include flex_align_center;

            img {
                width: 50px;
                height: 50px;
            }
        }

        nav {
            @include flex_align_center;
            padding-top: 1.5rem;

            ul {

                display: flex;

                li {
                    text-transform: uppercase;
                    margin-right: 1.7rem;

                    a {
                        color: black;
                        padding-bottom: 2rem;
                        display: block;
                        font-size: .7rem;
                        font-weight: 500;


                        &:hover {
                            color: $primary_color;
                        }
                    }

                    .active {
                        color: $primary_color;
                        border-bottom: 4px solid rgb(2, 130, 249);
                    }
                }
            }

        }
    }


}

.jumbotron {
    width: 100%;
    height: 17rem;

    img {
        width: 100%;
        height: 100%;
        display: block;
        object-fit: cover;
        object-position: top;
    }
}
</style>