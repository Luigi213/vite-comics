<script>
export default {
    name: 'header',
    data() {
        return {
            listNavbar: [
                {
                    type: 'CHARACTERS ',
                    active: false,
                },
                {
                    type: 'COMICS',
                    active: true,
                },
                {
                    type: 'MOVIES',
                    active: false,
                },
                {
                    type: 'TV',
                    active: false,
                },
                {
                    type: 'COLLECTIBLES',
                    active: false,
                },
                {
                    type: 'VIDEOS',
                    active: false,
                },
                {
                    type: 'GAMES',
                    active: false,
                },
                {
                    type: 'FANS',
                    active: false,
                },
                {
                    type: 'NEWS',
                    active: false,
                },
                {
                    type: 'SHOP',
                    active: false,
                },                
            ]
        }
    },
}
</script>
<template>
    <header>
        <div class="container">
            <div class="row">
                <div class="col-content">
                    <div class="image">
                        <img src="../assets/images/dc-logo.png" alt="logo">
                    </div>
                    <ul>
                        <li v-for="(listname, index) in listNavbar" :key="index" :class="listname.active ? 'active' : ''">
                            <a href="/">{{ listname.type }}</a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </header>
</template>
<style lang="scss">
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins' as *;
    header{
        .col-content{
            margin: 15px;
            @include display;
            .image{
                width: 80px;
                height: 80px;
                @include display;
            }
            ul{
                display: flex;
                li{
                    padding: 1rem;
                    &.active a,&:hover a{
                        color: $primary;
                        border-bottom: 5px solid $primary ;
                    }
                    a{  
                        padding-bottom: 43px ;
                        color: $secondary;                        
                        font-size: 10px;
                        font-weight: 600;
                    }
    
                }
            }
        }
    }
</style>