<template class="container">
    <div class="container">
        <h2>Ebenezer's Hobbies</h2>
        <div v-if="blok" class="card">
            <img src="https://a-us.storyblok.com/f/1015969/998x998/fb49add844/profile.png" alt="">
            <h2>{{ blok.title}}</h2>
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
    .template{
        margin: 0 auto;
       
    }
    .card{
        margin-left: 2rem;
    }

    img{
        width: 400px;
        margin-left: 10em;
        margin-bottom: 2em;;
    }

    p{
        font-size: medium;
        line-height: 2em;
    }

    .container{
        padding: 5em;
        margin-left: 5em;
    }

    h2{
        /* margin-left: 5em; */
        margin-bottom: 2em;
    }


</style>