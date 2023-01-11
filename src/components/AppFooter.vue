<script>
export default {
    name: 'footer',
    data() {
        return {
            cards: [
                {
                    images: 'buy-comics-digital-comics.png',
                    title: 'DIGITAL COMICS'
                },
                {
                    images: 'buy-comics-merchandise.png',
                    title: 'DC MERCHANDISE'
                },
                {
                    images: 'buy-comics-subscriptions.png',
                    title: 'SUBSCRIPTION'
                },
                {
                    images: 'buy-comics-shop-locator.png',
                    title: 'COMIC SHOP LOCATOR'
                },
                {
                    images: 'buy-dc-power-visa.svg',
                    title: 'DC POWER VISA'
                },
            ]
        }
    },
}
</script>
<template>
    <footer>
        <section class="bg-footer-nav">
            <div class="container-footer">
                <div class="card" v-for="(card,index) in cards" :key="index">
                    <div class="card-image">
                        <img :src="`/src/assets/images/${card.images}`">
                    </div>
                    <span>{{ card.title }}</span>                    
                </div>
            </div>
        </section>
        <section class="middle-footer">
            <div class="container">
                <div class="row-footer-middle">
                    <div class="info">
                        <h3>DC COMICS</h3>
                        <ul>
                            <li><a href="/">Characters</a> </li>
                            <li><a href="/">Comics</a> </li>
                            <li><a href="/">Movies</a> </li>
                            <li><a href="/">TV</a> </li>
                            <li><a href="/">Games</a> </li>
                            <li><a href="/">Videos</a></li>
                            <li><a href="/">News</a> </li>
                        </ul>
                        <h3>SHOP</h3>
                        <ul>
                            <li><a href="/">Shop DC</a> </li>
                            <li><a href="/">Shop DC Collectibles</a> </li>
                        </ul>
                    </div>
                    <div class="info">
                        <h3>DC</h3>
                        <ul>
                            <li><a href="/">Terms Of Use</a> </li>
                            <li><a href="/">Privacy policy (New)</a> </li>
                            <li><a href="/">Ad Choices</a> </li>
                            <li><a href="/">Advertising</a> </li>
                            <li><a href="/">Jobs</a> </li>
                            <li><a href="/"> Subscriptions</a></li>
                            <li><a href="/">Talent Workshops</a> </li>
                            <li><a href="/">CPSC Certificates</a> </li>
                            <li><a href="/">Ratings</a> </li>
                            <li><a href="/">Shop Help</a> </li>
                            <li><a href="/">Contact Us</a> </li>
                        </ul>
                    </div>
                    <div class="info">
                        <h3>SITES</h3>
                        <ul>
                            <li><a href="/">DC</a> </li>
                            <li><a href="/">MAD Magazin</a> </li>
                            <li><a href="/">DC Kids</a> </li>
                            <li><a href="/">DC Universe</a> </li>
                            <li><a href="/">DC Power Visa</a> </li>
                        </ul>
                    </div>
                </div>
            </div>
        </section>
        <section class="bottom-footer">
            <div class="container">
                <div class="row-footer-bottom">
                    <button>SIGN-UP NOW</button>
                    <div class="icons">
                        <h3>FOLLOW US</h3>
                        <div class="icon">
                            <img src="../assets/images/footer-facebook.png" alt="logo-facebook">
                            <img src="../assets/images/footer-twitter.png" alt="logo-twitter">
                            <img src="../assets/images/footer-youtube.png" alt="logo-youtube">
                            <img src="../assets/images/footer-pinterest.png" alt="logo-pinterest">
                            <img src="../assets/images/footer-periscope.png" alt="logo-periscope">
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </footer>
</template>
<style lang="scss">
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins' as *;
    footer{
        .bg-footer-nav{
            background-color: $primary ;
            .container-footer{
                width: 72%;
                margin: 0 auto;
                padding: 20px 0;
                display: flex;
                .card{                
                    width: calc(100% / 5);
                    @include align;
                    &:last-child .card-image{
                        margin-right: 10px 
                    }
                    span{
                        width: 50%;
                        font-size: 11px;
                        color: $tertiary;
                    }
                    .card-image{ 
                        @include cardSize;
                    }
                }
            }
        }
        .middle-footer{
            background: url(../assets/images/footer-bg.jpg);
            background-repeat: no-repeat;
            background-size: cover;
            display: flex;
            .row-footer-middle{
                display: flex;
                .info{
                    margin: 2rem 2rem 4rem 0;
                    h3{
                        color: $tertiary;
                        margin: 1rem 0;
                    }
                    ul
                    {
                        li a{
                            @include infoList                
                        }
                    }
                }
            }
            .container {
                background: url(../assets/images/dc-logo-bg.png);
                background-repeat: no-repeat;
                background-position: right;
            }
        }
        .bottom-footer{
            background-color: #303030;
            padding: 2rem 0;
            .row-footer-bottom{
                @include display;
                button{
                    border:2px solid $primary ;
                    color: $tertiary;
                    padding: 1rem;
                    font-size: 20px;
                    cursor: pointer;
                }
                .icons{
                    width: 33%;
                    color: $primary;
                    @include display;
                    h3{
                        font-size: 17px;
                    }
                    .icon{
                        img{
                            padding-left: 1rem;
                        }
                    }
                }
            }
        }
    }
</style>