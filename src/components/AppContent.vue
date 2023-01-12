<script>
export default {
    data() {
        return {

        }
    }
}
</script>
<template lang="">
    <main>
        <div class="main_container">
            <h2>-- Content goes here --</h2>
        </div>
    </main>
</template>
<style lang="scss">
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

main {
    background-color: rgb(28, 28, 28);

    .main_container {
        @include main_center;
        padding: 2rem;

        h2 {
            color: $color_white;
        }
    }
}
</style>