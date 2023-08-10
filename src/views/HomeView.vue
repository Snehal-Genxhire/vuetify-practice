<template>
  <Cards />
  <ButtonsAndIcons />
  <TextAndColors />
  <ChipsAndDividers />
  <Dialogs />
  <Lists />
  <Grids />
  <Appbars />
  <BottomNavigation />
  <Sidebar />
  <Paginations />
  <Carousel />
  <ExpantionPanel />
  <Menus />
  <Overlays/>
  <Sheets/>
  <Tooltip/>
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
    Tooltip
},
};
</script>
