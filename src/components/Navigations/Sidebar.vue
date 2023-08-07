<template>
  <v-app-bar color="primary">
    <v-app-bar-nav-icon
      variant="text"
      @click="drawer = !drawer"
    ></v-app-bar-nav-icon>
    <v-app-bar-title>Dashboard</v-app-bar-title>
    <v-spacer></v-spacer>
    <v-btn variant="text" icon="mdi-heart"></v-btn>
    <v-btn variant="text" icon="mdi-magnify"></v-btn>
    <v-btn variant="text" icon="mdi-dots-vertical"></v-btn>
  </v-app-bar>

  <v-navigation-drawer v-model="drawer" location="bottom" temporary>
    <v-list>
      <v-list-item
        v-for="item in items"
        :key="item.title"
        :title="item.title"
      ></v-list-item>
    </v-list>
  </v-navigation-drawer>

  <v-main class="pa-4"> 
    <v-card-text class="pa-0"
      >Lorem ipsum dolor sit amet consectetur adipisicing elit. Nisi ipsam iusto
      fugit maiores ducimus dolore at cum repellat reiciendis
      fugiat.</v-card-text
    >
  </v-main>


  <v-card max-width="250">
    <v-layout>
      <v-navigation-drawer
        expand-on-hover
        rail
      >
        <v-list>
          <v-list-item
            prepend-avatar="https://avataaars.io/?avatarStyle=Transparent&topType=ShortHairShortCurly&accessoriesType=Prescription02&hairColor=Bl"
            title="John"
            subtitle="john_a88@gmailcom"
          ></v-list-item>
        </v-list>

        <v-divider></v-divider>

        <v-list density="compact" nav>
          <v-list-item prepend-icon="mdi-folder" title="My Files" value="myfiles"></v-list-item>
          <v-list-item prepend-icon="mdi-account-multiple" title="Shared with me" value="shared"></v-list-item>
          <v-list-item prepend-icon="mdi-star" title="Starred" value="starred"></v-list-item>
        </v-list>
      </v-navigation-drawer>

      <v-main style="height: 250px"></v-main>
    </v-layout>
  </v-card>
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
      items: [
        {
          title: "Foo",
          value: "foo",
        },
        {
          title: "Bar",
          value: "bar",
        },
        {
          title: "Fizz",
          value: "fizz",
        },
        {
          title: "Buzz",
          value: "buzz",
        },
      ],
    };
  },
};
</script>