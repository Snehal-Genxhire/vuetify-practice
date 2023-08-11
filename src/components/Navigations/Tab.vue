<template>
  <h2 class="text-center ma-5">Tabs</h2>
  <v-container fluid>
    <v-row>
      <v-col cols="6">
        <v-card width="700" class="ma-3">
          <v-tabs align-tabs="center" v-model="tab" color="primary">
            <v-tab value="one" prepend-icon="mdi-home">First Tab</v-tab>
            <v-tab value="two" prepend-icon="mdi-heart">Second Tab</v-tab>
            <v-tab value="three" prepend-icon="mdi-access-point"
              >thired Tab</v-tab
            >
          </v-tabs>
          <v-card-text>
            <v-window v-model="tab">
              <v-window-item value="one">
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolores
                accusantium, omnis consequuntur ea voluptate sapiente reiciendis
                alias cupiditate iusto corrupti!
              </v-window-item>
              <v-window-item value="two">
                Lorem ipsum dolor sit amet consectes alias cupiditate iusto
                corrupti!
              </v-window-item>
              <v-window-item value="three">
                Lorem ipsum dolor sit amet upiditate iusto corrupti!
              </v-window-item>
            </v-window>
          </v-card-text>
        </v-card>
      </v-col>

      <v-col cols="6">
        <v-card>
          <v-toolbar color="primary">
            <v-app-bar-nav-icon></v-app-bar-nav-icon>
            <v-toolbar-title>Dashboard</v-toolbar-title>
            <v-btn icon="mdi-heart"></v-btn>
            <v-btn icon="mdi-dots-vertical"></v-btn>

            <template v-slot:extension>
              <v-tabs v-model="tab1">
                <v-tab v-for="item in items" :key="item" :value="item"
                  >{{ item }}
                </v-tab>
              </v-tabs>
            </template>
          </v-toolbar>

          <v-window v-model="tab1">
            <v-window-item v-for="item in items" :key="item" :value="item">
              <v-card flat>
                <v-card-text>{{ text }}</v-card-text>
              </v-card>
            </v-window-item>
          </v-window>
        </v-card>
      </v-col>
    </v-row>
  </v-container>

  <v-card width="800" class="mx-auto mt-5">
    <v-tabs v-model="tab3" align-tabs="end" color="pink">
      <v-tab :value="1">Landscape</v-tab>
      <v-tab :value="2">City</v-tab>
      <v-tab :value="3">Abstract</v-tab>
    </v-tabs>

    <v-window v-model="tab3">
      <v-window-item v-for="n in 3" :key="n" :value="n">
        <v-container fluid>
          <v-row>
            <v-col cols="12" md="4" v-for="i in 6" :key="i">
              <v-img
                :src="`https://picsum.photos/500/300?image=${i * n * 5 + 6}`"
                :lazy-src="`https://picsum.photos/10/6?image=${i * n * 5 + 10}`"
                aspect-ratio="1"
              ></v-img>
            </v-col>
          </v-row>
        </v-container>
      </v-window-item>
    </v-window>
  </v-card>

  <v-card width="1000" class="mx-auto">
    <v-tabs v-model="tab4" bg-color="pink-lighten-2">
      <v-tab v-for="n in length" :key="n" :value="n">Item{{ n }}</v-tab>
    </v-tabs>

    <v-card-actions>
        <v-btn @click="length--" :disabled="!length">Remove Item</v-btn>
        <v-btn @click="length++">Add Item</v-btn>
    </v-card-actions>
  </v-card>



</template>
<script>
export default {
  data() {
    return {
        length:8,
      tab: null,
      tab1: null,
      tab3: null,
      tab4: null,
      items: ["web", "shopping", "videos", "images", "news"],
      text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
    };
  },
  watch:{
    length(v){
        this.tab4 = v - 1
    }
  }
};
</script>