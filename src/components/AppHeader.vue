<script>
export default {
    data() {
        return {
            navBar: [
                {
                    item:'CHARACTER'
                },
                {
                    item:'COMICS'
                },
                {
                    item:'MOVIES'
                },
                {
                    item:'TV'
                },
                {
                    item:'GAMES'
                },
                {
                    item:'COLLECTIBLES'
                },
                {
                    item:'VIDEOS'
                },
                {
                    item:'FANS'
                },
                {
                    item:'NEWS'
                },
                {
                    item:'SHOP'
                },
            ]
        };
    },
    methods: {

    }
}
</script>

<template>
    <header>
        <div>
            <img src="/public/img/dc-logo.png" alt="Logo">
        </div>
        <nav>
            <ul>
                <li v-for="(singleItem, i) in navBar">{{ singleItem.item }}</li>
            </ul>
        </nav>
    </header>
</template>

<style lang="scss" scoped>

@use '../assets/scss/partials/mixins.scss' as *;
@use '../assets/scss/partials/variables.scss' as *;

header {
    
    @include container;
    @include row;
    @include flex-center;
    justify-content: space-between;
    height: 100px;

    div {
        @include img-container;
        margin: $space-20;

        img {
            @include full-size;
        }

    }

    
    nav {
        height: 100%;

        ul {
        @include row;
        @include full-size;
        @include flex-center;

            li {
                display: block;
                margin: 0 $space-10;

                // SISTEMARE HEIGHT DEI LI CHE NON OCCUPA IL 100%

                &:hover {
                    color: $main-color;
                    cursor: pointer;
                    border-bottom: 3px solid $main-color;
                }
            }
        }
    }    
    
}
</style>
