<template>
  <v-tabs align-tabs="center" v-model="tab" color="primary">
    <v-tab value="1">cards</v-tab>
    <v-tab value="2">Buttons</v-tab>
    <v-tab value="3">Text</v-tab>
    <v-tab value="4">Chips & Dividers</v-tab>
    <v-tab value="5">Dialogs</v-tab>
    <v-tab value="6">Lists</v-tab>
    <v-tab value="7">Grids</v-tab>
    <v-tab value="8">Tooltip </v-tab>
    <v-tab value="9">Carousel </v-tab>
    <v-tab value="10">ExpantionPanel </v-tab>
    <v-tab value="11">Menus </v-tab>

    <v-tab value="12">Overlays </v-tab>
    <v-tab value="13">Sheets </v-tab>
    <v-tab value="14">Selection</v-tab>
    <v-tab value="15">Feedback </v-tab>
    <v-tab value="16">Navigation </v-tab>
  </v-tabs>

  <v-window v-model="tab">
    <v-window-item value="1">
      <Cards />
    </v-window-item>
    <v-window-item value="2">
      <ButtonsAndIcons />
    </v-window-item>
    <v-window-item value="3">
      <TextAndColors />
    </v-window-item>
    <v-window-item value="4">
      <ChipsAndDividers />
    </v-window-item>
    <v-window-item value="5">
      <Dialogs />
    </v-window-item>
    <v-window-item value="6">
      <Lists />
    </v-window-item>

    <v-window-item value="7">
      <Grids />
    </v-window-item>

    <v-window-item value="8">
      <Tooltip />
    </v-window-item>

    <v-window-item value="9"> <Carousel /></v-window-item>

    <v-window-item value="10"><ExpantionPanel /> </v-window-item>
    <v-window-item value="11"><Menus /> </v-window-item>

    <v-window-item value="12"> <Overlays /></v-window-item>

    <v-window-item value="13"> <Sheets /></v-window-item>
    <v-window-item value="14">
<ButtonToggle/>
    </v-window-item>
    <v-window-item value="15">
     <Feedback/>
    </v-window-item>

    <v-window-item value="16">
      <BottomNavigation />
      <Appbars />
      <Sidebar />
      <BreadCrumbs />
      <Tab />
      <Paginations
    /></v-window-item>
  </v-window>

  
</template>

<script>
import ButtonsAndIcons from "@/components/ButtonsAndIcons.vue";
import TextAndColors from "@/components/TextAndColors.vue";
import Cards from "@/components/Cards.vue";
import ChipsAndDividers from "@/components/ChipsAndDividers.vue";
import Dialogs from "@/components/Dialogs.vue";
import Lists from "@/components/Lists.vue";
import Grids from "@/components/Grids.vue";
import Appbars from "@/components/Navigations/Appbars.vue";
import BottomNavigation from "@/components/Navigations/BottomNavigation.vue";
import Sidebar from "@/components/Navigations/Sidebar.vue";
import Paginations from "@/components/Navigations/Paginations.vue";
import Carousel from "@/components/Carousel.vue";
import ExpantionPanel from "@/components/ExpantionPanel.vue";
import Menus from "@/components/Menus.vue";
import Overlays from "@/components/Overlays.vue";
import Sheets from "@/components/Sheets.vue";
import Tooltip from "@/components/Tooltip.vue";
import BreadCrumbs from "@/components/Navigations/BreadCrumbs.vue";
import Tab from "@/components/Navigations/Tab.vue";
import ButtonToggle from "@/components/Selection/ButtonToggle.vue";
import Feedback from "@/components/Feedback.vue";

export default {
  name: "HomeView",
  components: {
    TextAndColors,
    ButtonsAndIcons,
    Cards,
    ChipsAndDividers,
    Dialogs,
    Lists,
    Grids,
    Appbars,
    BottomNavigation,
    Sidebar,
    Paginations,
    Carousel,
    ExpantionPanel,
    Menus,
    Overlays,
    Sheets,
    Tooltip,
    BreadCrumbs,
    Tab,
    ButtonToggle,
    Feedback
},
  data() {
    return {
      tab: null,
    };
  },
};
</script>
