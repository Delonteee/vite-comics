<script>

import AppComicCard from './AppComicCard.vue';

export default {
    data() {
        return {
            comics:[
                {
                    "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book",
                },
                {
                    "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book",
                },
                {
                    "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel",
                },
                {
                    "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel",
                },
            ]
        };
    },
    
    components: {
        AppComicCard,
    },
    methods: {

    }
}
</script>

<template>
    <main>
        <section>
            <div>
                <div class="jumbotron-container">
                    <div class="button-absolute-container">
                        <h3 class="series-title">
                            Current Series
                        </h3>
                    </div>
                </div>
            </div>
        </section>

        <section class="main-gray">
            <div>
                <AppComicCard v-for="(singleComic, i) in comics" :key="i" :comic="singleComic"/>
            </div>
            
            <div class="main-button-container">
                <button class="main-button">
                    Load More
                </button>
            </div>
        </section>
    </main>
</template>

<style lang="scss" scoped>

@use '../assets/scss/partials/mixins.scss' as *;
@use '../assets/scss/partials/variables.scss' as *;

main{

    padding: $space-50  0;
    background-color: #1C1C1C;
    width: 100%;
    color: white;

    >div{
        width: 100% auto;
        height: 400px;
        background-image: url('/public/img/jumbotron.jpg');
        background-position: top center;
        object-fit: cover;
        background-repeat: no-repeat;
        
        .jumbotron-container{
            @include container;
            position: relative;
            height: 100%;
        }

        .button-absolute-container{
            position: absolute;
            bottom: -20px;
            left: -20px;

            .series-title{
                background-color: $main-color;
                padding: $space-10 $space-20;
                text-transform: uppercase;
                color: white;
                font-weight: $text-bold;
            }
        }
    }
    .main-gray{
        background-color: white;
        padding: $space-50;
        
        >div:first-child{
            @include container;
            @include row;
        }
        .main-button-container{
            text-align: center;

            .main-button{
                background-color: $main-color;
                border: none;
                font-size: $text-large;
                padding: $space-10 $space-50;
                text-transform: uppercase;
                color: white;
                font-weight: $text-bold;
            }
        }
    }
}

main {
    
    padding: $space-50  0;
    background-color: #1C1C1C;
    width: 100%;

    section {
    }
}
</style>
