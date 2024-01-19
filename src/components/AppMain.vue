<script>
export default {
    data() {
        return {

        };
    },
    methods: {

    }
}
</script>

<template>
    <main>
        <section>
            --> Content goes here <--
        </section>
    </main>
</template>

<style lang="scss" scoped>

@use '../assets/scss/partials/mixins.scss' as *;
@use '../assets/scss/partials/variables.scss' as *;

main {
    padding: $space-50  0;
    background-color: #1C1C1C;
    width: 100%;

    section {
        @include container;
        color: white;
    }
}
</style>
