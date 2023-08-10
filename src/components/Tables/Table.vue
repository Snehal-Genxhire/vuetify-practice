<template>
  <h2 class="text-center">Tables</h2>
  <div class="d-flex">
    <v-card width="500" class="ma-5">
      <v-table hover>
        <thead>
          <tr>
            <th class="text-black">Name</th>
            <th class="text-black">Calories</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="item in desserts" :key="item.neme">
            <td>{{ item.name }}</td>
            <td>{{ item.calories }}</td>
          </tr>
        </tbody>
      </v-table>
    </v-card>

    <v-card width="500" class="ma-5">
      <v-table theme="dark" height="400px" fixed-header hover>
        <thead>
          <tr>
            <th>Name</th>
            <th>Calories</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="item in desserts" :key="item.neme">
            <td>{{ item.name }}</td>
            <td>{{ item.calories }}</td>
          </tr>
        </tbody>
      </v-table>
    </v-card>
  </div>
  <v-card width="800">
    <v-data-table
      :headers="headers"
      :items-per-page="itemPerPage"
      :items="desserts"
      height="500"
      fixed-footer
      fixed-header
      hover
      v-model="selected"
      item-value="name"
      loading-text
      show-select
      return-object
      item-selectable="selectable"
      select-strategy="all"
      v-model:sort-by="sortBy"
    >
    </v-data-table>
    <v-card>
      <pre>{{ selected }}</pre>
    </v-card>
  </v-card>

  <h3 class="text-center">V-data-table-pagination</h3>

  <v-card>
    <v-row class="ma-5">
      <v-col cols="4">
        <v-text-field
          placeholder="Search"
          prepend-icon="mdi-magnify"
          v-model="search"
        ></v-text-field>
      </v-col>
    </v-row>
  </v-card>
  <v-data-table
    :items="desserts"
    :custom-filter="FilterOnlyCaps"
    :headers="headers"
    :page="page"
    :search="search"
    :items-per-page="itemPerPage"
    hide-default-footer
  >
    <template v-slot:bottom>
      <v-pagination :length="pageCount" v-model="page"> </v-pagination>
    </template>
  </v-data-table>
</template>

<script>
export default {
  data() {
    return {
      search: "",
      page: 1,
      sortBy: [{ key: "calories", order: "asc" }],
      itemPerPage: 5,
      selected: [],
      headers: [
        {
          title: "Dessert (100g serving)",
          align: "start",
          sortable: false,
          key: "name",
        },
        { title: "Calories", align: "end", key: "calories" },
        { title: "Fat (g)", align: "end", key: "fat" },
        { title: "Carbs (g)", align: "end", key: "carbs" },
        { title: "Protein (g)", align: "end", key: "protein" },
        { title: "Iron (%)", align: "end", key: "iron" },
      ],
      desserts: [
        {
          name: "Frozen Yogurt",
          calories: 159,
          fat: 6.0,
          carbs: 24,
          protein: 4.0,
          iron: "1",
        },
        {
          name: "Jelly bean",
          calories: 375,
          fat: 0.0,
          carbs: 94,
          protein: 0.0,
          iron: "0",
          selectable: false,
        },
        {
          name: "KitKat",
          calories: 518,
          fat: 26.0,
          carbs: 65,
          protein: 7,
          iron: "6",
          selectable: false,
        },
        {
          name: "Eclair",
          calories: 262,
          fat: 16.0,
          carbs: 23,
          protein: 6.0,
          iron: "7",
        },
        {
          name: "Gingerbread",
          calories: 356,
          fat: 16.0,
          carbs: 49,
          protein: 3.9,
          iron: "16",
        },
        {
          name: "Ice cream sandwich",
          calories: 237,
          fat: 9.0,
          carbs: 37,
          protein: 4.3,
          iron: "1",
        },
        {
          name: "Lollipop",
          calories: 392,
          fat: 0.2,
          carbs: 98,
          protein: 0,
          iron: "2",
        },
        {
          name: "Cupcake",
          calories: 305,
          fat: 3.7,
          carbs: 67,
          protein: 4.3,
          iron: "8",
        },
        {
          name: "Honeycomb",
          calories: 408,
          fat: 3.2,
          carbs: 87,
          protein: 6.5,
          iron: "45",
        },
        {
          name: "Donut",
          calories: 452,
          fat: 25.0,
          carbs: 51,
          protein: 4.9,
          iron: "22",
        },
      ],
    };
  },

  methods: {
    FilterOnlyCaps(value, query, item) {
      return (
        value != null &&
        query != null &&
        typeof value === "string" &&
        value.toString().toLocaleUpperCase().indexOf(query) !== -1
      );
    },
  },
  computed: {
    pageCount() {
      return Math.ceil(this.desserts.length / this.itemPerPage);
    },
  },
};
</script>
