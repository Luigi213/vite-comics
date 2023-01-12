<script>
export default {
    name: 'main'
}
</script>
<template>
    <main>
        <div class="container">
            <h1>Content goes here</h1>
        </div>
    </main>
</template>
<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins' as *;
    main{
        background-color: #1C1C1C ;
        h1{
            padding: 5rem 2rem;
            color: $tertiary
        }
    }
</style>