<script>
export default {
    props:{
        dcImage: Object
    } 
}
</script>
<template>
    <div class="card">
        <div class="card-image">
            <img :src="dcImage.thumb" :alt="dcImage.series">
        </div>
        {{dcImage.series}}
    </div>
</template>
<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
    .card{
        color: $tertiary;
        width: calc(100% / 6 - 30px);
        margin: 20px 15px 30px 15px;
        .card-image{
            margin-bottom: 1rem;
            img{
                width: 100%;
                height: 175px;
                object-fit: cover;
                object-position: top;
            }
        }
    }
</style>