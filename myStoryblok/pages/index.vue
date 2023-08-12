
<template>
    <div class="body">
        <h1>Ebenezer's Story</h1>
        <!-- <Teaser :body="story.body" /> -->
        <template v-for="block in story.body" :key="block._uid">
        <Hobbies v-if="block.component === 'Hobbies'" :blok="block" />
        <Teaser v-if="block.component === 'teaser'" :blok="block" />
        <Inspiration v-if="block.component === 'Inspiration'" :blok="block" />     
</template>
    </div>
</template>

<script>
  export default {
      data: function(){
          return{
              story:''
          }
      },
      created: function() {
          fetch('https://api-us.storyblok.com/v2/cdn/stories/home?version=draft&token=BFBL3zjTUh6EvXDGaIeFFwtt&cv=1691786686')
          .then(resp => resp.json())
          .then(data => this.story = data.story.content)
      }
  }
</script>