<template>
    <div class="layout-gallery">
        <img id="photo1" src="../../assets/photo1.png" alt="Gallery Photo 1">
        <img id="photo2" src="../../assets/photo2.png" alt="Gallery Photo 2">
        <img id="photo3" src="../../assets/photo3.png" alt="Gallery Photo 3">
        <img id="photo4" src="../../assets/photo4.png" alt="Gallery Photo 4">
        <img id="photo5" src="../../assets/photo5.png" alt="Gallery Photo 5">
        <img id="photo6" src="../../assets/photo6.png" alt="Gallery Photo 6">
    </div>
</template>

<script>
    export default {
        name: "Gallery"
    }
</script>

<style lang="scss" scoped>
    @import "../../scss/variables";
    @import "../../scss/breakpoints";

    .layout-gallery {
        flex: 1;

        width: 100%;
        max-width: 900px;

        display: grid;
        align-self: center;
        grid-template: "a b b" 1fr
                       "c c d" 1fr
                       "e f d" 1fr / 1fr 1fr 1fr;
        gap: 1.6vw;

        @include breakpoint('s') {

        }
    }

    img {
        width: 100%;
        height: 100%;
        border-radius: 12px;
        filter: drop-shadow(0px 4px 6px rgba(0, 0, 0, 0.15));
    }

    #photo1 {
        grid-area: a;
    }

    #photo2 {
        grid-area: b;
    }

    #photo3 {
        grid-area: c;
    }

    #photo4 {
        grid-area: d;
    }

    #photo5 {
        grid-area: e;
    }

    #photo6 {
        grid-area: f;
    }

</style>