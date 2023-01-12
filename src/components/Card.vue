<script>
export default {

    props: {
        img: String,
        title: String
    }

}
</script>
<template>
    <div class="card">
        <div class="thumb">
            <img :src="img" alt="img">
        </div>
        <h4>{{ title }}</h4>
    </div>
</template>
<style lang="scss">
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

.card {

    width: calc((80vw / 6) - 1rem);
    margin: 0 .5rem 2rem .5rem;

    .thumb {

        img {
            object-fit: cover;
            width: 100%;
            height: calc((80vw / 6) - 1rem);
            object-position: top;
            display: block;

            &:hover {
                filter: brightness(50%);
            }
        }
    }

    h4 {
        margin-top: 1rem;
        text-transform: uppercase;
        color: $color_white;
        font-size: .8rem;
    }
}
</style>