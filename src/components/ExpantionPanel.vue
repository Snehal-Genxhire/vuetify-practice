<template>
  <h2 class="text-center ma-4">Expansion Panel</h2>
  <v-row>
    <v-col cols="4">
        <div class="text-subtitle-2 mb-2">Default</div>
      <v-expansion-panels color="deep-purple-lighten-4">
        <v-expansion-panel
          v-for="i in 3"
          :key="i"
          expand-icon="mdi-plus"
          collapse-icon="mdi-minus"
          title="Item"
          text="Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor 
      incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation 
      ullamco laboris nisi ut aliquip ex ea commodo consequat."
        ></v-expansion-panel>
      </v-expansion-panels>
    </v-col>

    <v-col cols="4">
        <div class="text-subtitle-2 mb-2">Accordion</div>
        <v-expansion-panels variant="accordion" disabled theme="dark">
            <v-expansion-panel
            v-for="i in 3"
            :key="i"
            title="disabled"
            text="Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor 
      incididunt ut labore et dolore magna aliqua."
            ></v-expansion-panel>
        </v-expansion-panels>
    </v-col>
    <v-col cols="4">
        <div class="text-subtitle-2 mb-2">Inset</div>
        <v-expansion-panels variant="inset" color="amber-lighten-3" >
            <v-expansion-panel
            v-for="i in 3"
            :key="i"
            title="Item"
            text="Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor 
      incididunt ut labore et dolore magna aliqua."
            ></v-expansion-panel>
        </v-expansion-panels>
    </v-col>
    <v-col cols="4">
        <div class="text-subtitle-2 mb-2">popout</div>
        <v-expansion-panels variant="popout">
            <v-expansion-panel
            v-for="i in 3"
            :key="i"
            title="Item"
            text="Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor 
      incididunt ut labore et dolore magna aliqua."
            ></v-expansion-panel>
        </v-expansion-panels>
    </v-col>
  </v-row>
</template>