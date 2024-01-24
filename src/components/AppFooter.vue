<script>
export default {
    data() {
        return {
            dcComics: [
                {
                    title: 'Characters'
                },
                {
                    title: 'Comics'
                },
                {
                    title: 'Movies'
                },
                {
                    title: 'TV'
                },
                {
                    title: 'Games'
                },
                {
                    title: 'Videos'
                },
                {
                    title: 'News'
                },
            ],
            shop: [
               {
                    title: 'Shop DC'
                }, 
                {
                    title: 'Shop DC Collectibles'
                },
            ],
            dc: [
                {
                    title:'Terms of use'
                },
                {
                    title:'Privacy policy (New)'
                },
                {
                    title:'Ad Choices'
                },
                {
                    title:'Advertising'
                },
                {
                    title:'Jobs'
                },
                {
                    title:'Subscriptions'
                },
                {
                    title:'Talent Workshops'
                },
                {
                    title:'CPSC Certificates'
                },
                {
                    title:'Ratings'
                },
                {
                    title:'Shop Help'
                },
                {
                    title:'Contact Us'
                },
            ],
            sites: [
                {
                    title:'DC'
                },
                {
                    title:'MAD Magazin'
                },
                {
                    title:'DC Kids'
                },
                {
                    title:'DC Universe'
                },
                {
                    title:'DC Power Visa'
                },
            ]
        };
    },
    methods: {

    }
}
</script>

<template>
    <footer>
        <section id="footer-top">
            <div class="foot-img-container">            
                <div>   
                    <div class="foot-list">
                        <h4>DC COMICS</h4>
                        <ul>
                            <li v-for="(singleElem, i) in dcComics"> {{ singleElem.title }}</li>
                        </ul>                       
                        <h4>SHOP</h4>
                        <ul>
                            <li v-for="(singleElem, j) in shop">{{ singleElem.title }}</li>
                        </ul>
                    </div>               
                    <div class="foot-list">
                        <h4>DC</h4>
                        <ul>
                            <li v-for="(singleElem, z) in dc">{{ singleElem.title }}</li>
                        </ul>
                    </div>
                    <div class="foot-list">
                        <h4>SITES</h4>
                        <ul>
                            <li v-for="(singleElem, x) in sites">{{ singleElem.title }}</li>
                        </ul>
                    </div>
                    <div class="overflow-logo">
                        <img src="/public/img/dc-logo-bg.png" alt="Logo Background">
                    </div>
                </div>
            </div>
        </section>

        <section id="footer-bottom">
            <div>
                <div>
                    <button class="foot-button">
                        SIGN UP NOW!
                    </button>
                </div>
                
                <div class="lower-foot-icon">
                    <h2>FOLLOW US</h2>
                    <ul>
                        <li><img src="/public/img/footer-facebook.png" alt="Facebook icon"></li>
                        <li><img src="/public/img/footer-twitter.png" alt="Twitter icon"></li>
                        <li><img src="/public/img/footer-youtube.png" alt="Youtube icon"></li>
                        <li><img src="/public/img/footer-pinterest.png" alt="Pinterest icon"></li>
                        <li><img src="/public/img/footer-periscope.png" alt="Periscope icon"></li>
                    </ul>
                </div>
            </div>
        </section>
    </footer>
</template>

<style lang="scss" scoped>

@use '../assets/scss/partials/mixins.scss' as *;
@use '../assets/scss/partials/variables.scss' as *;

footer {

    background-image: url('/public/img/footer-bg.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    height: 400px;

    #footer-top {
        @include container;        
        .foot-img-container {

            >div {
                @include row;               
                .foot-list {
                    margin-right: $space-20;
                    margin-top: $space-20;
                    h4 {
                        color: white;
                        margin: $space-20 0;
                    }
                    ul {
                        list-style: none;
                        color:grey;
                    }
                }

                .overflow-logo{
                    overflow: hidden;
                    display: flex;
                    align-items: center;
                    height: 400px;
                    img{
                        height: 150%;
                        display: block;
                    }
                }
            }
        }
    }

    #footer-bottom {
        padding: $space-30;
        background-color: #303030;
        >div {
            @include container;
            @include row;
            @include flex-center;
            justify-content: space-between;
            
            .foot-button {
                font-family: 'Oswald', sans-serif;
                background-color: #303030;
                border: 2px solid $main-color;
                font-size: $text-large;
                color: white;
                padding: $space-10;
            }
            .lower-foot-icon {
                @include row;
                align-items: center;
                color: $main-color;
                ul {
                    @include row;
                    list-style: none;
                    li {
                        padding: $space-10;
                    }
                }
            }
        }
    }
}

</style>
