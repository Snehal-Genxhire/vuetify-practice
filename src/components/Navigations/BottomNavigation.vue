<template>
    <h2 class="text-center">Bottom Navigations</h2>
    <v-btn class="text-red" @click="active = !active">Toggle Botton Nav</v-btn>
    <v-bottom-navigation grow
    v-model="value"
    :active="active"
    :bg-color="color"
    elevation="9"
    rounded
    color="primary">
        <v-btn > <v-icon icon="mdi-history"></v-icon> Recent</v-btn>
        <v-btn > <v-icon icon="mdi-heart"></v-icon>Favorites</v-btn>
        <v-btn > <v-icon icon="mdi-map-marker"></v-icon> Nearby</v-btn>
    </v-bottom-navigation>
</template>

<script>
export default {
    data(){
        return{
            value:2,
            active: false,
        }
    },

    computed:{
        color(){
            switch(this.value){
                case 0 : return 'pink-lighten-4'
                case 1: return 'orange-lighten-2'
                case 2: return 'indigo-lighten-4'
                default: return 'indigo-lighten-4'
            }
        }
    }
}
</script>