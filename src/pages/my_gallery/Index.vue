<template>
    <div class="main-layout" >
        <Profile v-bind:srcProfilePicture="srcProfilePicture"/>
        <Gallery/>
        <Footer/>
    </div>
</template>

<script>
    import Footer from "@/components/Footer";
    import Profile from "@/pages/my_gallery/Profile";
    import Gallery from "@/pages/my_gallery/Gallery";
    export default {
        name: "Index",
        components: {Footer, Gallery, Profile},
        data() {
            return {
                srcProfilePicture: "../../assets/photo1.png",
                bite: "bitsdfsdfe"
            }
        }
    }
</script>

<style lang="scss" scoped>
    @import "../../scss/breakpoints";
    @import "../../scss/variables";

    .main-layout {
        display: flex;
        flex-direction: column;
        min-height: 100vh;
        row-gap: 50px;

        background-color: $color-background;
        max-width: 1680px;
        margin: auto;
        padding: $padding-large;

        @include breakpoint('s') {
            padding: $padding-small;
        }
    }
</style>