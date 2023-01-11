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
                    <img src="../assets/images/dc-logo.png" alt="logo">
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
            @include displayHeader;
            margin: 2rem 0;
            ul{
                list-style: none;
                display: flex;
                li{
                    padding: 1rem;
                    &.active a,&:hover a{
                        color: $primary;
                        border-bottom: 5px solid $primary ;
                    }
                    a{  
                        padding-bottom: 42px ;
                        color: $secondary;                        
                        text-decoration: none;
                        font-size: 13px;
                        font-weight: 600;
                    }
    
                }
            }
        }
    }
</style>