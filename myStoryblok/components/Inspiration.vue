<template>
    <div class="container">
        <h2>Ebenezer's Inspiration</h2>
        <div v-if="blok" class="card">
            <img src="https://a-us.storyblok.com/f/1015969/3840x2160/7af329f298/cibo-desktop.png" alt="">
            <!-- <h2>{{ blok.title}}</h2> -->
            <p>{{ blok.Description }}</p>
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