<template>
    <div class="layout-profile">
        <img class="profile-picture" src="../../assets/profilePhoto.png" alt="Profile Picture"/>
        <div>
            <p class="name">Rodney Cotton</p>
            <p class="location">Helsinki, Finland</p>
        </div>
        <div class="layout-counters" >
            <div v-bind:key="counter" v-for="counter in counters">
                <CounterDisplay v-bind:counter="counter" v-bind:label="counter.label" v-bind:count="counter.count"/>
            </div>
        </div>
    </div>
</template>

<script>
    import CounterDisplay from "@/pages/my_gallery/CounterDisplay";
    export default {
        name: "Profile",
        components: {CounterDisplay},
        data() {
            return {
                counters: [
                    {
                        label: "Posts",
                        count: "100"
                    },
                    {
                        label: "Follower",
                        count: "2,242"
                    },
                    {
                        label: "Following",
                        count: "1,432"
                    }
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
    @import "../../scss/variables";
    @import "../../scss/breakpoints";

    .layout-profile {
        display: flex;
        flex-direction: column;
        align-items: center;
        row-gap: 20px;
    }

    .profile-picture {
        max-width: 156px;
        min-width: 100px;
        width: 20vw;
        border-radius: 16px;
    }

    p {
        font-family: $font-family-primary;
        font-weight: 600;
        text-align: center;
    }

    .name {
        font-size: $font-size-large;
        font-weight: 600;
        color: $color-gray-1;

        @include breakpoint('s') {
            font-size: $font-size-regular;
        }
    }

    .location {
        font-size: $font-size-regular;
        font-weight: 600;
        color: $color-gray-2;

        @include breakpoint('s') {
            font-size: $font-size-very-small;
        }
    }

    .layout-counters {
        display: flex;
        align-items: center;
        justify-content: center;
        flex-wrap: wrap;

        gap: 24px;

        @include breakpoint('s') {
            gap: 12px;
        }
    }
</style>