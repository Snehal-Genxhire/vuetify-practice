<template>
  <h1 class="ma-2 text-center">Lists</h1>
  <div class="d-flex">
    <v-card max-width="300" class="ma-5">
      <v-card-text>One line list</v-card-text>
      <v-list lines="one" bg-color="pink" rounded>
        <v-list-item
          v-for="item in items"
          :key="item.text"
          :title="item.text"
          active-color="black"
          :value="item"
          :subtitle="item.subtext"
        >
        </v-list-item>
      </v-list>
    </v-card>

    <v-card max-width="400" class="ma-5">
      <v-card-text>two lines</v-card-text>
      <v-list lines="two">
        <v-list-item
          v-for="item in items"
          :key="item.text"
          :title="item.text"
          :subtitle="item.subtext"
          :value="item"
          color="primary"
          rounded="shaped"
        ></v-list-item>
      </v-list>
    </v-card>

    <v-card max-width="300" height="320" class="ma-5">
      <v-list density="compact" nav bg-color="grey-lighten-3">
        <v-list-item
          v-for="item in navItems"
          :key="item.text"
          :value="item"
          color="orange"
          rounded="xl"
        >
          <template v-slot:prepend
            ><v-icon :icon="item.icon"></v-icon
          ></template>
          <v-list-item-title v-text="item.text"></v-list-item-title>
        </v-list-item>
      </v-list>
    </v-card>

    <v-card max-width="600" max-height="600" class="ma-5">
      <v-list nav>
        <v-list-item prepend-icon="mdi-home" title="Home"></v-list-item>
        <v-list-group value="Users" fluid>
          <template v-slot:activator="{ props }">
            <v-list-item v-bind="props" title="User" prepend-icon="mdi-account">
            </v-list-item>
          </template>

          <v-list-group fluid>
            <template v-slot:activator="{ props }">
              <v-list-item title="Admin" v-bind="props"></v-list-item>
            </template>

            <v-list-item
              v-for="([title, icon], i) in admins"
              :key="i"
              :title="title"
              :prepend-icon="icon"
              :value="title"
            ></v-list-item>
          </v-list-group>

          <v-list-group fluid>
            <template v-slot:activator="{ props }">
              <v-list-item v-bind="props" title="Actions"></v-list-item>
            </template>

            <v-list-item
              v-for="([title, icon], i) in cruds"
              :key="i"
              :title="title"
              :prepend-icon="icon"
              :value="title"
            ></v-list-item>
          </v-list-group>
        </v-list-group>
      </v-list>
    </v-card>
  </div>

  <v-card max-width="700" class="ma-5">
    <v-toolbar color="secondary">
      <v-btn icon="mdi-menu" variant="text"></v-btn>
      <v-toolbar-title>My Files</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn icon="mdi-magnify" variant="text"></v-btn>
      <v-btn icon="mdi-view-module"></v-btn>
    </v-toolbar>

    <v-list lines="two">
      <v-list-subheader inset>Folders</v-list-subheader>
      <v-list-item
        v-for="item in folders"
        :key="item.title"
        :title="item.title"
        :subtitle="item.subtitle"
        :value="item.title"
      >
        <template v-slot:prepend>
          <v-avatar color="grey-lighten-1">
            <v-icon color="white" icon="mdi-folder"></v-icon>
          </v-avatar>
        </template>

        <template v-slot:append>
          <v-avatar>
            <v-icon icon="mdi-information"></v-icon>
          </v-avatar>
        </template>
      </v-list-item>
      <v-divider inset></v-divider>
      <v-list-subheader inset>Files</v-list-subheader>
      <v-list-item
        v-for="file in files"
        :key="file.title"
        :title="file.title"
        :subtitle="file.title"
        :color="file.color"
        :value="file.title"
      >
    <template v-slot:prepend>
       <v-avatar :color="file.color"><v-icon color="white">{{file.icon }}</v-icon></v-avatar>
    </template>

    <template v-slot:append>
        <v-avatar><v-icon icon="mdi-information"></v-icon></v-avatar>
    </template>
</v-list-item>
    </v-list>
  </v-card>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          text: "Item 1",
          subtext:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi, ratione debitis quis est labore voluptatibus! Eaque cupiditate minima, at placeat totam, magni doloremque veniam neque porro libero rerum unde voluptatem!",
        },
        {
          text: "Item 2",
          subtext:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi, ratione debitis quis est labore",
        },
        {
          text: "Item 3",
          subtext:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi, ratione debitis quis est labore",
        },
        {
          text: "Item 4",
          subtext:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi, ratione debitis quis est labore",
        },
      ],
      navItems: [
        { text: "My Files", icon: "mdi-folder" },
        { text: "Shared with me", icon: "mdi-account-multiple" },
        { text: "Starred", icon: "mdi-star" },
        { text: "Recent", icon: "mdi-history" },
        { text: "Offline", icon: "mdi-check-circle" },
        { text: "Uploads", icon: "mdi-upload" },
        { text: "Backups", icon: "mdi-cloud-upload" },
      ],
      open: ["Users"],
      admins: [
        ["Management", "mdi-account-multiple-outline"],
        ["Settings", "mdi-cog-outline"],
      ],
      cruds: [
        ["Create", "mdi-plus-outline"],
        ["Read", "mdi-file-outline"],
        ["Update", "mdi-update"],
        ["Delete", "mdi-delete"],
      ],
      files: [
        {
          color: "blue",
          icon: "mdi-clipboard-text",
          subtitle: "Jan 20, 2014",
          title: "Vacation itinerary",
        },
        {
          color: "amber",
          icon: "mdi-gesture-tap-button",
          subtitle: "Jan 10, 2014",
          title: "Kitchen remodel",
        },
      ],
      folders: [
        {
          subtitle: "Jan 9, 2014",
          title: "Photos",
        },
        {
          subtitle: "Jan 17, 2014",
          title: "Recipes",
        },
        {
          subtitle: "Jan 28, 2014",
          title: "Work",
        },
      ],
    };
  },
};
</script>