<template>
  <h1 class="text-center">Grids</h1>

  <v-container fluid>
    <v-row v-for="n in 2" :key="n">
      <v-col v-for="n in 20" :key="n"
        ><v-sheet color="blue-lighten-3" class="text-center pa-2"
          >Grid</v-sheet
        ></v-col
      >
    </v-row>
  </v-container>

  <h2 class="text-center">Alignment</h2>
  <v-container fluid>
    <v-row>
      <v-col align-self="start"
        ><v-sheet color="yellow">Align-self-start</v-sheet></v-col
      >
      <v-col align-self="center"
        ><v-sheet color="yellow">Align-self-center</v-sheet></v-col
      >
      <v-col align-self="end" cols="2"
        ><v-sheet color="yellow">Align-self-end</v-sheet></v-col
      >
    </v-row>

    <v-row justify="end">
      <v-col v-for="n in 2" :key="n" cols="2">
        <v-sheet class="pa-2 ma-2" color="orange">justify-end </v-sheet>
      </v-col>
    </v-row>

    <v-row justify="center">
      <v-col v-for="n in 2" :key="n" cols="2"
        ><v-sheet class="pa-2 ma-2" color="orange"
          >justify center</v-sheet
        ></v-col
      >
    </v-row>

    <v-row justify="start">
      <v-col v-for="n in 2" :key="n" cols="2"
        ><v-sheet class="pa-2 ma-2" color="orange"
          >justify center</v-sheet
        ></v-col
      >
    </v-row>
    <v-row justify="space-between">
      <v-col v-for="n in 2" :key="n" cols="2"
        ><v-sheet class="pa-2 ma-2" color="orange"
          >justify space between</v-sheet
        ></v-col
      >
    </v-row>
  </v-container>

  <v-container>
    <v-row no-gutters>
      <v-col cols="12"><v-sheet class="pa-2" color="blue">no-glutter v-col-12 </v-sheet></v-col>
      <v-col cols="6"><v-sheet class="pa-2" color="blue">v-col-6</v-sheet></v-col>
    </v-row>
  </v-container>

  <v-container>
    <v-row >
      <v-col cols="3"><v-sheet class="pa-2" color="blue">spacer </v-sheet></v-col>
      <v-spacer></v-spacer>
      <v-col cols="3"><v-sheet class="pa-2" color="blue">spacer</v-sheet></v-col>
    </v-row>
  </v-container>
</template>