<template>
  <h2 class="text-center">Range sliders</h2>
  <v-container fluid>
    <v-row>
      <v-col cols="3">
        <v-card max-width="100" color="grey-lighten-2" class="ma-5">
          <v-range-slider
            class="pt-5"
            color="indigo"
            append-icon="mdi-home"
            direction="vertical"
          ></v-range-slider>
        </v-card>
      </v-col>
      <v-col cols="3">
        <v-card max-width="400" color="grey-lighten-2" class="ma-5">
          <v-range-slider
            color="orange"
            focused
            class="pt-5"
            max="20"
            rounded
            show-ticks
            min="1"
            append-icon="mdi-home"
          ></v-range-slider>
        </v-card>
      </v-col>
      <v-col cols="3"> </v-col>
    </v-row>
  </v-container>
  <v-card color="grey-lighten-2" class="ma-5">
    <v-range-slider
      color="orange"
      focused
      class="pt-5 align-center"
      rounded
      :min="-15"
      :max="15"
      :step="1"
      hide-details
      v-model="range"
      show-ticks
      thumb-label="always"
    >
      <template v-slot:prepend>
        <v-text-field
          :model-value="range[0]"
          single-line
          hide-details
          type="number"
          variant="outlined"
          label="min"
          style="width: 70px;"
          @change="$set(range, 0, $event)"

        >
        </v-text-field>
      </template>

      <template v-slot:append>
        <v-text-field
          :model-value="range[1]"
          single-line
          hide-details
          variant="outlined"
          style="width: 70px;"
          type="number"
          @change="$set(range, 1, $event)"
        ></v-text-field>
      </template>
    </v-range-slider>
  </v-card>

  <v-row>
    <v-col cols="12">
        <v-range-slider
        :ticks="seasons"
        :model-value="[0,1]"
        min="0"
        max="3"
        step="1"
        thumb-label="always"
        show-ticks="always"
        tick-size="4"
        >
        <template v-slot:thumb-label="{ modelValue }">
          <v-icon theme="dark" :icon="season(modelValue)"></v-icon>
        </template>
    </v-range-slider>
    </v-col>
  </v-row>
</template>

<script>
export default {
  data() {
    return {
      range: [-10, 10],
      seasons: {
        0: 'Winter',
        1: 'Spring',
        2: 'Summer',
        3: 'Fall',
      },
      icons: [
        'mdi-snowflake',
        'mdi-leaf',
        'mdi-fire',
        'mdi-water',
      ],
    };
  },
  methods: {
      season (val) {
        return this.icons[val]
      },
    },
};
</script>