<template>
    <v-container v-editable="blok">
      <v-layout align-center>
        <v-flex>
          <h1>{{blok.headline}}</h1>
          <h2>{{blok.subheadline}}</h2>
          <img :src="blok.image" alt="">
        </v-flex>
      </v-layout>
    </v-container>
</template>

<script>
export default {
  props: {
    blok: Object
  }
}
</script>

<style>
img {
  max-width: 100px;
}
</style>
