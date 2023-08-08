<template>
  <h2 class="text-center">Sliders</h2>
  <v-slider
    track-color="yellow"
    thumb-color="green"
    :min="0"
    :max="10"
    step="2"
    thumb-label
  ></v-slider>
  <v-slider
  prepend-icon="mdi-volume-high"
  ></v-slider>


</template>

<script>
  export default {
    data () {
      return {
        slider: 50,
        satisfactionEmojis: ['😭', '😢', '☹️', '🙁', '😐', '🙂', '😊', '😁', '😄', '😍'],
      }
    },
  }
</script>