<template>
  <!-- option 1 -> using the v-editable on a wrapper element as Vueitfy does not allow additional properties -->
  <v-carousel v-editable="blok">
    <v-carousel-item v-for="(image, i) in blok.images" :key="i" :src="image.filename"></v-carousel-item>
  </v-carousel>
</template>

<script>
export default {
  props: {
    blok: Object // content of that one instance loaded on Storyblok
  }
}
</script>