<template>
  <h2 class="text-center ma-5">Tooltips</h2>
  <v-container>
    <v-row>
      <v-col cols="3">
        <v-tooltip text="Hello!" eagar>
          <template v-slot:activator="{ props }">
            <v-btn v-bind="props">Tooltip</v-btn></template
          >
        </v-tooltip>
      </v-col>
      <v-col cols="3">
        <v-btn>
            start
          <v-tooltip activator="parent" text="Hello again!" scroll-strategy="reposition" location="start"></v-tooltip>
        </v-btn>
      </v-col>
      <v-col cols="3">
        <v-btn>
            Top
          <v-tooltip activator="parent" text="Hello top!" scroll-strategy="reposition" location="top"></v-tooltip>
        </v-btn>
      </v-col>
      <v-col cols="3">
        <v-btn>
            bottom
          <v-tooltip activator="parent" text="Hello bottom!" scroll-strategy="reposition" location="bottom"></v-tooltip>
        </v-btn>
      </v-col>
    </v-row>
  </v-container>
</template>