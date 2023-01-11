<script>
export default {
    name: 'main'
}
</script>
<template>
    <main>
        <div>
            <h1>Content goes here</h1>
        </div>
    </main>
</template>
<style lang="scss">
    @use '../styles/partials/variables' as *;
    main{
        background-color: #1C1C1C ;
        h1{
            padding: 5rem;
            color: $tertiary
        }
    }
</style>