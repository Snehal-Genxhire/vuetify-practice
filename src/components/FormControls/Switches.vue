<template>
  <h2 class="text-center">Switches</h2>
  <v-row>
    <v-col cols="2">
      <v-switch
        color="green"
        direction="vertical"
        error
        false-icon="mdi-close"
        hint="turn on!"
        persistent-hint
        large
      ></v-switch>
    </v-col>
    <v-col cols="2">
      <v-switch color="green" inset label="turn on/off" loading></v-switch>
    </v-col>
    <v-col cols="2">
      <div>{{ person }}</div>
      <v-switch
        indeterminate
        v-model="person"
        value="snehal"
        label="snehal"
      ></v-switch>
      <v-switch
        indeterminate
        v-model="person"
        value="Divya"
        label="Divya"
      ></v-switch>
      <v-switch
        indeterminate
        v-model="person"
        value="shubham"
        label="shubham"
      ></v-switch>
    </v-col>
    <v-col cols="2">
      <v-switch :model-value="true" color="blue" label="on"></v-switch>
    </v-col>
    <v-col cols="2">
      <v-switch
        :model-value="true"
        loading="error"
        color="blue"
        label="on"
      ></v-switch>
    </v-col>
    <v-col cols="2">
      <v-switch
        color="blue"
        v-model="switchMe"
      >
    <template v-slot:label>
        Turn on progress
        <v-progress-circular size="24" class="ms-2" :indeterminate="switchMe">
        </v-progress-circular>
    </template>
    </v-switch>
    </v-col>
  </v-row>
</template>

<script>
export default {
  data() {
    return {
      person: [],
      switchMe: false,
    };
  },
};
</script>