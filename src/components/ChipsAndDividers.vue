<template>
  <h1 class="ma-2 text-center">Chips</h1>
  <v-chip prepend-icon="mdi-cat" closable append-icon="mdi-star"> chip </v-chip>

  <v-chip color="red" closable draggable label class="ma-5">
    <v-icon start icon="mdi-tag"></v-icon>
    Colored
  </v-chip>
  <v-chip prepend-icon="mdi-twitter" color="blue" closable size="x-large" filter
    >New Tweet</v-chip
  >
  <v-chip append-icon="mdi-star" color="orange" class="ma-5" size="large"
    >Premium</v-chip
  >
  <v-chip append-icon="mdi-cake-variant" color="indigo">1 Year</v-chip>

  <h1 class="ma-2 text-center">Divider</h1>
  <v-divider color="error" inset thickness="10"></v-divider>
  <v-divider color="orange" class="ma-5" :thickness="18" vertical></v-divider>

  <v-card max-width="300" class="ma-5" color="red-lighten-4">
    <v-card-subtitle>Today</v-card-subtitle>
   
        <v-list-item subtitle="Hello" title="Snehal KAnase" >
            <template v-slot:prepend><v-icon icon="mdi-account" color="blue" size="large" class="mr-4"></v-icon></template>
            <v-chip prepend-icon="mdi-cake-variant" class="mt-2" size="small" color="indigo">Happy Birthday</v-chip>
        </v-list-item>

        <v-divider inset class="mt-3" color="black"></v-divider>
        <v-list-item subtitle="Hello" title="Snehal KAnase" >
            <template v-slot:prepend><v-icon icon="mdi-account" color="blue" size="large" class="mr-4"></v-icon></template>
            <v-chip prepend-icon="mdi-cake-variant" class="mt-2" size="small" color="indigo">Happy Birthday</v-chip>
        </v-list-item>
  
  </v-card>
</template>