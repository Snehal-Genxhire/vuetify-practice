<template>
  <h2 class="text-center">Alert</h2>
  <v-row>
    <v-col cols="4">
      <v-alert
        title="Error"
        type="error"
        closable
        variant="tonal"
        border="start"
        text="Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi, ratione debitis quis est labore voluptatibus! Eaque cupiditate minima, at placeat totam, magni doloremque veniam neque porro libero rerum unde voluptatem!"
      ></v-alert>
    </v-col>
    <v-col cols="4">
      <v-alert
        title="warning"
        type="warning"
        closable
        variant="outlined"
        border="top"
        text="Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi, ratione debitis quis est labore voluptatibus! Eaque cupiditate minima, at placeat totam, magni doloremque veniam neque porro libero rerum unde voluptatem!"
      ></v-alert>
    </v-col>
    <v-col cols="4">
      <v-alert
        title="Success"
        type="success"
        closable
        variant="tonal"
        border="bottom"
        text="Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi, ratione debitis quis est labore voluptatibus! Eaque cupiditate minima, at placeat totam, magni doloremque veniam neque porro libero rerum unde voluptatem!"
      ></v-alert>
    </v-col>
  </v-row>
</template>