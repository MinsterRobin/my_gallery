<template>
    <div class="layout-display">
        <p class="count">{{count}}</p>
        <p class="label">{{label}}</p>
    </div>
</template>

<script>
    export default {
        name: "CounterDisplay",
        props: ['count', 'label']
    }
</script>

<style lang="scss" scoped>
    @import "../../scss/breakpoints";
    @import "../../scss/variables";

    .layout-display {
        display: flex;
        flex-direction: column;

        align-items: center;
        justify-content: center;

        padding: 14px 24px;

        background: $color-gray-4;
        border-radius: 12px;

        @include breakpoint('s') {
            padding: 10px 15px;
        }
    }

    p {
        font-family: $font-family-primary;
        font-weight: 600;
    }

    .count {
        color: $color-gray-1;
        font-size: $font-size-medium;

        @include breakpoint('s') {
            font-size: $font-size-small;
        }
    }

    .label {
        color: $color-gray-3;
        font-size: $font-size-regular;

        @include breakpoint('s') {
            font-size: $font-size-small;
        }
    }

</style>