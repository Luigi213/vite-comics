<script>
export default {
    props:{
        dcImage: Object
    } 
}
</script>
<template lang="">
    <div class="card">
        {{ dcImage.series }}
    </div>
</template>
<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins' as *;
    .card{
        color: $tertiary
    }
</style>