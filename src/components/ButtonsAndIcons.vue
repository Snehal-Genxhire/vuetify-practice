<template>
    <h1 class="ma-3 text-center">Buttons</h1>
    <v-btn class="ma-5">Button</v-btn>
    <v-btn variant="outlined" class="ma-5">outlined Button</v-btn>
    <v-btn variant="tonal" class="ma-5">Tonal Button</v-btn>
    <v-btn variant="text" class="ma-5">Text Button</v-btn>
    <v-btn variant="plain" class="ma-5">Plain Button</v-btn>
    <v-btn color="green" class="ma-5">Colored Button</v-btn>

    <v-btn density="comfortable" class="ma-5">comfortable Density</v-btn>
    <v-btn block class="bg-indigo-lighten-5">Block Button</v-btn>

    <v-btn disabled class="ma-5" elevation="5">Disabled & elevation</v-btn>
    <v-btn flat class="ma-5 text-red">Flat</v-btn>

    <v-btn :loading="loading" @click="load" class="ma-5 text-blue">Loading</v-btn>

    <v-btn rounded>Rounded Button</v-btn>
    <v-btn rounded="lg" class="ma-5 bg-yellow-lighten-4">Rounded LG</v-btn>

    <v-btn size="small" class="ma-5">Small Btn</v-btn>
    <v-btn size="large" class="ma-5">Large Btn</v-btn>

    <v-btn :ripple="false">Without Ripple</v-btn>

    <v-btn :loading="loading" @click="load"> Cudtomize loader
        <template v-slot:loader>
            <v-progress-linear indeterminate class="text-blue"></v-progress-linear>
        </template>
    </v-btn>

    <h1 class="ma-3 text-center">Icons</h1>

    <v-btn icon="mdi-email" class="text-green ma-5"></v-btn>
    <v-btn icon="mdi-open-in-new" size="large" class="ma-5"></v-btn>
    <v-btn icon="mdi-account" class="text-blue d-none d-md-flex d-lg-none"></v-btn>

    <v-btn
    append-icon="mdi-account-circle"
    prepend-icon="mdi-check-circle"
    class="ma-5 d-none d-lg-flex">
    <template v-slot:prepend>
        <v-icon color="success"></v-icon>
    </template>
    Button
    <template v-slot:append>
        <v-icon color="warning"></v-icon>
    </template>
    </v-btn>
</template>

<script> 
 export default {
 data(){
    return{
        loading: false,
    }
 },
 methods:{
    load(){
        this.loading= true,
        setTimeout(() => (this.loading = false), 1000)
    }
 }
 }
</script>