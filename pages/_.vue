<template>
  <main class="main">
    <h1>Story loaded: {{story.name}}</h1>
    
    <template v-if="story.content.component">
      <component :key="story._uid" :blok="story.content" :is="story.content.component"></component>
    </template>
  </main>
</template>

<script>
export default {
   mounted() {
    this.$storybridge.on(['input', 'published', 'change'], (event) => {
      if (event.action == 'input') {
        if (event.story.id === this.story.id) {
          // Push story into current story of data
          this.story = event.story
        }
      } else if (!event.slugChanged) {
        // Reload the page on save events
        window.location.reload()
      }
    })
  },
  data() {
    return {
      story: {
        content: {}
      }
    }
  },
  async asyncData(context) {
    // check for / and load /home entry.
    let currentPath = context.route.path == '/' ? '/home' : context.route.path

    let storyResponse = await context.app.$storyapi.get('cdn/stories/' + currentPath, {
      version: 'draft'
    })

    return storyResponse.data
  }
}
</script>

<style>
</style>
