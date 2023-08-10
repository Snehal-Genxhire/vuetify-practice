<template>
  <h2 class="text-center">Text Fields</h2>
  <v-row>
    <v-col cols="2">
      <v-text-field
        label="text"
        prepend-inner-icon="mdi-account"
        color="indigo"
      ></v-text-field>
    </v-col>
    <v-col cols="2">
      <v-text-field prefix="$" label="ammount" type="number"></v-text-field>
    </v-col>
    <v-col cols="2">
      <v-text-field
        suffix="@gmail.com"
        label="Email"
        type="email"
      ></v-text-field>
    </v-col>
    <v-col cols="5">
      <v-text-field
        label="Message"
        v-model="message"
        type="input"
        :append-icon="message ? 'mdi-send' : 'mdi-microphone'"
        clearable
        :append-inner-icon="marker ? 'mdi-map-marker' : 'mdi-map-marker-off'"
        @click:append-inner="toggleMarker"
        @click:append="clearMessage"
      >
        <template v-slot:prepend
          ><v-icon
            color="amber-lighten-1"
            size="24"
            class="bg-black rounded-circle"
            @click="toggleIcons"
            >{{ icon }}</v-icon
          ></template
        >
      </v-text-field>
    </v-col>
  </v-row>
</template>

<script>
export default {
  data() {
    return {
      message: "",
      marker: true,
      iconIndex: 0,
      icons: [
        "mdi-emoticon",
        "mdi-emoticon-cool",
        "mdi-emoticon-dead",
        "mdi-emoticon-excited",
        "mdi-emoticon-happy",
        "mdi-emoticon-neutral",
        "mdi-emoticon-sad",
        "mdi-emoticon-tongue",
      ],
    };
  },
  methods: {
    toggleMarker() {
      this.marker = !this.marker;
    },
    toggleIcons() {
      this.iconIndex === this.icons.length - 1
        ? (this.iconIndex = 0)
        : this.iconIndex++;
    },
    clearMessage(){
       this.message = ''
    }
  },
  computed: {
    icon() {
      return this.icons[this.iconIndex];
    },
  },
};
</script>