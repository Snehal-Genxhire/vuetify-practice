<template>
  <h2 class="text-center">Menu</h2>
  <v-row>
    <v-col cols="4">
      <v-menu open-on-hover theme="dark" transition="scale-transition">
        <template v-slot:activator="{ props }">
          <v-btn v-bind="props" color="primary">Activate slot</v-btn>
        </template>
        <v-list>
          <v-list-item
            v-for="(item, i) in items"
            :key="i"
            :title="item.title"
          ></v-list-item>
        </v-list>
      </v-menu>
    </v-col>

    <v-col cols="4">
      <v-menu open-on-hover theme="dark" transition="slide-y-transition">
        <template v-slot:activator="{ props }">
          <v-btn v-bind="props" color="primary">Activate slot</v-btn>
        </template>
        <v-list>
          <v-list-item
            v-for="(item, i) in items"
            :key="i"
            :title="item.title"
          ></v-list-item>
        </v-list>
      </v-menu>
    </v-col>

    <v-col cols="4">
      <v-menu open-on-hover theme="dark" transition="slide-x-transition">
        <template v-slot:activator="{ props }">
          <v-btn v-bind="props" color="primary">Activate slot</v-btn>
        </template>
        <v-list>
          <v-list-item
            v-for="(item, i) in items"
            :key="i"
            :title="item.title"
          ></v-list-item>
        </v-list>
      </v-menu>
    </v-col>
  </v-row>
</template>

<script>
export default {
  data: () => ({
    items: [
      { title: "Click Me" },
      { title: "Click Me" },
      { title: "Click Me" },
      { title: "Click Me 2" },
    ],
  }),
};
</script>