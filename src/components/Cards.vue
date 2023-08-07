<template>
  <h1 class="ma-5 text-center">Cards</h1>
  <div class="d-flex justify-center bg-yellow-lighten-4">
    <v-card
      variant="outlined"
      title="Outlined Card with Props"
      text="rem, ipsum dolor sit amet consectetur adipisicing eli"
      subtitle="subtitle"
      max-width="300"
      class="ma-5"
    ></v-card>

    <v-card loading max-width="300" class="ma-5">
      <v-card-items>
        <v-card-title>Card with Markup</v-card-title>
        <v-card-subtitle>Subtitle</v-card-subtitle>
        <v-card-text
          >Lorem, ipsum dolor sit amet consectetur adipisicing elit. Sed,
          ea.</v-card-text
        >
      </v-card-items>
    </v-card>

    <v-card variant="tonal" max-width="300">
      <template v-slot:title>Tonal Card with slots</template>
      <template v-slot:subtitle>subtitle</template>
      <template v-slot:text
        >Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestias,
        reprehenderit?</template
      >
    </v-card>
  </div>

  <div class="d-flex">
    <v-card
      max-width="400"
      class="ma-8"
      height="300"
      prepend-icon="mdi-home"
      append-icon="mdi-close"
      color="blue-lighten-3"
      elevation="9"
      href="/about"
      loading
    >
      <v-card-items>
        <v-card-title>Card with All Props</v-card-title>
        <v-card-subtitle>subtitle</v-card-subtitle>
      </v-card-items>
      <v-card-text
        >Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis
        facere quod quam eius animi eos placeat, minima dolorum veritatis
        nemo!</v-card-text
      >
      <v-card-actions>
        <v-btn>Click</v-btn>
      </v-card-actions>
    </v-card>

    <v-card
      class="ma-8"
      title="Twitter"
      max-width="400"
      color="grey-darken-3"
      height="220"
    >
      <template v-slot:prepend
        ><v-icon color="blue" icon="mdi-twitter"></v-icon
      ></template>
      <v-card-text
        >"Lorem ipsum dolor sit amet consectetur adipisicing elit. Nam accusamus
        magni nemo. Nulla dolores consequatur officiis illum nemo nostrum
        quaerat."</v-card-text
      >

      <v-card-actions class="pa-1">
        <v-list-item class="w-100">
          <template v-slot:prepend
            ><v-avatar
              class="ma-0"
              color="grey"
              image="https://avataaars.io/?avatarStyle=Transparent&topType=ShortHairShortCurly&accessoriesType=Prescription02&hairColor=Bl"
            ></v-avatar>
          </template>
          <v-card-title class="pb-0">John</v-card-title>
          <v-card-subtitle class="pt-0">Vue Developer</v-card-subtitle>

          <template v-slot:append>
            <div class="justify-end mt-2">
              <v-icon icon="mdi-heart" color="red" class="me-1"></v-icon>
              <span class="subheading me-2">34</span>
              <v-icon
                icon="mdi-share-variant"
                color="white"
                class="me-1"
              ></v-icon>
              <span class="me-1">12</span>
            </div>
          </template>
        </v-list-item>
      </v-card-actions>
    </v-card>

    <v-card width="400" class="ma-8 mx-auto" elevation="3 " :loading="loading">
      <v-card-text>
        <p>Word of the day</p>
        <p class="text-h4 text-primary">el·ee·mos·y·nar·y</p>
        <p class="text-disabled mt-4">adjective</p>
        <p class="mt-6">
          relating to or dependent on charity; charitable. "an eleemosynary
          educational institution."
        </p>
      </v-card-text>
      <v-card-actions>
        <v-btn class="text-green" variant="text" @click="onClick"
          >Learn More</v-btn
        >
      </v-card-actions>

      <v-expand-transition>
        <v-card v-if="reveal">
          <v-card-text>
            <p class="text-h5 text-black">Origin</p>
            <p class="ma-2">
              late 16th century (as a noun denoting a place where alms were
              distributed): from medieval Latin eleemosynarius, from late Latin
              eleemosyna ‘alms’, from Greek eleēmosunē ‘compassion’
            </p>
          </v-card-text>
          <v-card-actions>
            <v-btn variant="text" class="text-red" @click="reveal = false">Close</v-btn>
          </v-card-actions>
        </v-card>
      </v-expand-transition>
    </v-card>
  </div>
</template>

<script>
export default {
  data() {
    return {
      reveal: false,
      loading: false
    };
  },
  methods:{
    onClick(){
      this.reveal= true;
      this.loading = true;

      setTimeout(() => {
        this.loading= false
      }, 1000);
    }
  }
};
</script>