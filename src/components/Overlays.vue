<template>
    <h2 class="text-center ma-5">Overlays</h2>
    <p class="text-center ma-2">Creates a dimmed layer over the application</p>

    <v-btn @click="overlay = !overlay">Show overlay</v-btn>
    <v-overlay v-model="overlay"></v-overlay>

    <v-btn>
        Block
        <v-overlay
        activator="parent"
        scroll-strategy="block"
        location-strategy="connected">
        <v-card class="pa-2">
            Hello
        </v-card>
        </v-overlay>
    </v-btn>
    <v-btn>
        close
        <v-overlay
        activator="parent"
        scroll-strategy="close"
        location-strategy="connected">
        <v-card class="pa-2">
            Hello
        </v-card>
        </v-overlay>
    </v-btn>
  
    <v-btn>
        reposition
        <v-overlay
        activator="parent"
        scroll-strategy="reposition"
        location-strategy="connected">
        <v-card class="pa-2">
            Hello
        </v-card>
        </v-overlay>
    </v-btn>

    <v-btn id="btn">None</v-btn>
    <v-overlay activator="#btn" location-strategy="connected" scroll-strategy="none"><v-card class="pa-2">Hello</v-card></v-overlay>
</template>

<script>
export default {
    data(){
        return{
            overlay: false,
        }
    }
}
</script>