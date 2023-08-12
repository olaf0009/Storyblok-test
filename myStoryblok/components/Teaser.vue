<template>
    <div class="container">
        <h2>Welcome to my World</h2>
        <div v-if="blok" class="card">
            <p>{{ blok.headline }}</p>
        </div>
    </div>

</template>

<script>
    export default {
        props:['blok']
    }
</script>

<style>
    .card{
        margin-left: 2rem;
    }
</style>