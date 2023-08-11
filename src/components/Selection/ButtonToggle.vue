<template>
  <h2 class="text-center">Button Toggle</h2>
  <v-card class="ma-5">
    <v-row>
    <v-col cols="3">
      <v-btn-toggle>
        <v-btn icon="mdi-format-align-left"></v-btn>
        <v-btn icon="mdi-format-align-center"></v-btn>
        <v-btn icon="mdi-format-align-right"></v-btn>
        <v-btn icon="mdi-format-align-justify"></v-btn>
      </v-btn-toggle>
    </v-col>

    <v-col cols="3"
      ><v-btn-toggle multiple v-model="toggleMultiple" class="ma-5">
        <h5>Multiple</h5>
        <v-btn icon="mdi-format-align-left"></v-btn>
        <v-btn icon="mdi-format-align-center"></v-btn>
        <v-btn icon="mdi-format-align-right"></v-btn>
        <v-btn icon="mdi-format-align-justify"></v-btn> </v-btn-toggle
    ></v-col>

    <v-col cols="3">
      <h4>Mandatory</h4>
      <v-btn-toggle mandatory shaped v-model="toggleMandatory" class="ma-5">
        <v-btn icon="mdi-format-align-left"></v-btn>
        <v-btn icon="mdi-format-align-center"></v-btn>
        <v-btn icon="mdi-format-align-right"></v-btn>
        <v-btn icon="mdi-format-align-justify"></v-btn> </v-btn-toggle
    ></v-col>
  </v-row>
  </v-card>
 
 <v-chip-group filter multiple selected-class="" v-model="selection">
  <v-chip>Firplace</v-chip>
  <v-chip>wahser</v-chip>
  <v-chip>dryer</v-chip>
  <v-chip>Dogs ok</v-chip>
  <v-chip>Cats ok</v-chip>
  <v-chip> Wheelchair access</v-chip>
 </v-chip-group>
</template>

<script>
export default {
  data() {
    return {
      toggleMultiple: null,
      toggleMandatory: null,
      selection: null
    };
  },
};
</script>