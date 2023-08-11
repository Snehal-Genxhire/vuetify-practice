<template>
  <h2 class="text-center ma-5">BreadCrumbs</h2>
  <v-row>
    <v-col cols="3">
      <v-breadcrumbs
        :items="['Home', 'Form', 'Tables']"
        bg-color="primary"
        disabled
      ></v-breadcrumbs>
    </v-col>
    <v-col cols="3">
      <v-breadcrumbs
        :items="['Home', 'Form', 'Tables']"
        divider="-"
        bg-color="info"
        color="black"
        rounded
      ></v-breadcrumbs>
    </v-col>
    <v-col cols="3">
      <v-breadcrumbs :items="['Home', 'Form', 'Tables']" bg-color="success">
        <template v-slot:divider
          ><v-icon icon="mdi-chevron-right"></v-icon></template
      ></v-breadcrumbs>
    </v-col>
  </v-row>
</template>

<script>
export default {
  data() {
    return {
      item: ["Home", "Form", "Tables"],
    };
  },
};
</script>