<template>
  <h2 class="text-center">AutoCompletes</h2>
  <div class="d-flex">
    <v-card width="300" height="55" class="ma-5">
      <v-autocomplete
        label="Choose one Country"
        clearable
        :items="items"
      ></v-autocomplete>
    </v-card>

    <v-card width="300" height="55" class="ma-5">
      <v-autocomplete
        multiple
        chips
        clearable
        :items="items"
        label="Choose Multiple Country"
      ></v-autocomplete>
    </v-card>

    <v-card width="300" height="55" class="ma-5">
      <v-autocomplete
        clearable
        chips
        variant="outlined"
        :items="items"
        label="outlined"
      ></v-autocomplete>
    </v-card>

    <v-card width="300" height="55" class="ma-5">
      <v-autocomplete
        clearable
        variant="solo-filled"
        label="solo-filled"
        :items="items"
      ></v-autocomplete>
    </v-card>
  </div>

  <v-container>
    <v-row>
      <v-col cols="4">
        <v-autocomplete
          label="solo"
          :items="items"
          variant="solo"
          clearable
          prepend-icon="mdi-earth"
        ></v-autocomplete>
      </v-col>
      <v-col cols="4">
        <v-autocomplete
          label="outlined"
          variant="outlined"
          clearable
          :items="items"
          closable-chips
          error-messages="erro"
          rounded
          validation-on="input"
          base-color="green"
          center-affix
          auto-select-first
          append-icon="mdi-earth"
        ></v-autocomplete>
      </v-col>
      <v-col cols="4">
        <v-autocomplete
          label="Default"
          clearable
          :items="items"
          chips
        ></v-autocomplete>
      </v-col>
    </v-row>
  </v-container>

  <v-card max-width="400" color="indigo" height="300">
    <v-toolbar color="indigo-darken-2" flat>
      <v-btn icon="mdi-account"></v-btn>
      <v-toolbar-title>User Profile</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn icon @click="isEditing = !isEditing">
        <v-fade-transieion>
          <v-icon v-if="isEditing">mdi-close</v-icon>
          <v-icon v-else>mdi-pencil</v-icon>
        </v-fade-transieion>
      </v-btn>
    </v-toolbar>

    <v-card-text>
      <v-text-field label="Name" :disabled="!isEditing"></v-text-field>
      <v-autocomplete
        label="Country"
        :items="items"
        :disabled="!isEditing"
        v-model="select"
        v-model:search="search"
        :loading="loading"
      ></v-autocomplete>
    </v-card-text>
    <v-divider></v-divider>
    <v-spacer></v-spacer>
    <v-btn variant="text" :disabled="!isEditing">Save</v-btn>
  </v-card>
</template>

<script>
export default {
  data() {
    return {
      isEditing: false,
      hasSaved: false,
      loading: false,
      select: null,
      search: null,
      items: ["India", "USA", "Japan", "England", "Rassia"],
    };
  },
};
</script>

