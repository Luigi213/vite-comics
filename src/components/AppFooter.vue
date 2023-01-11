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
                    <div class="icons">
                        <img :src="`/src/assets/images/${card.images}`">
                    </div>
                    <span>{{ card.title }}</span>                    
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
                width: 75%;
                margin: 0 auto;
                display: flex;
                .card{                
                    width: calc(100% / 5);
                    @include align;
                    &:last-child .icons{
                        margin-right: 10px 
                    }
                    span{
                        width: 50%;
                        font-size: 11px;
                        color: $tertiary;
                    }
                    .icons{ 
                        @include cardSize;
                    }
                }
            }
        }
    }
</style>