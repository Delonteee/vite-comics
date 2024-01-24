<script>
export default {
    data() {
        return {
            blueItems : [
                {
                    image: '/public/img/buy-comics-digital-comics.png',
                    caption: 'DIGITAL COMICS'
                },
                {
                    image: '/public/img/buy-comics-merchandise.png',
                    caption: 'DC MERCHANDISE'
                },
                {
                    image: '/public/img/buy-comics-subscriptions.png',
                    caption: 'SUBSCRIPTION'
                },
                {
                    image: '/public/img/buy-comics-shop-locator.png',
                    caption: 'COMIC SHOP LOCATOR'
                },
                {
                    image: '/public/img/buy-dc-power-visa.svg',
                    caption: 'DC POWER VISA'
                },
            ]
        };
    },
    methods: {

    }
}
</script>

<template>
    <section>
        <div id="blueSection">
            <div class="blue-img-sec" v-for="(singleElem, i) in blueItems">
                <div>
                    <img :src="singleElem.image" :alt="singleElem.caption">
                </div>
                <p>{{ singleElem.caption }}</p>
            </div>
        </div>
    </section>  
</template>

<style lang="scss" scoped>

@use '../assets/scss/partials/mixins.scss' as *;
@use '../assets/scss/partials/variables.scss' as *;

section {
    background-color: $main-color;
    #blueSection {
    padding: $space_50 10px;
    display: flex;
    justify-content: space-between;
    @include container;
        div {
            @include row;
            align-items: center;
            div {
                @include img-container;
                img {
                    @include full-size;
                    object-fit: contain;
                    display: block;
                }
            }
            p {
                color: white;
                padding-left: $space-10;
            }
        }
    }
}

</style>
