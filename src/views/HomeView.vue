<template>
  <!-- <Cards/>
  <ButtonsAndIcons/>
  <TextAndColors/>
  <ChipsAndDividers/>
  <Dialogs/>
  <Lists/>
  <Grids/>
  <Appbars/>
  <BottomNavigation/>
  <Sidebar/>
  <Paginations/> -->
  <Carousel/>
</template>

<script>
import ButtonsAndIcons from '@/components/ButtonsAndIcons.vue';
import TextAndColors from '@/components/TextAndColors.vue';
import Cards from '@/components/Cards.vue'
import ChipsAndDividers from '@/components/ChipsAndDividers.vue';
import Dialogs from '@/components/Dialogs.vue';
import Lists from '@/components/Lists.vue';
import Grids from '@/components/Grids.vue';
import Appbars from '@/components/Navigations/Appbars.vue';
import BottomNavigation from '@/components/Navigations/BottomNavigation.vue';
import Sidebar from '@/components/Navigations/Sidebar.vue';
import Paginations from '@/components/Navigations/Paginations.vue';
import Carousel from '@/components/Carousel.vue';

export default ({
  name: 'HomeView',
  components:{ TextAndColors, ButtonsAndIcons, Cards, ChipsAndDividers, Dialogs, Lists, Grids, Appbars, BottomNavigation, Sidebar, Paginations, Carousel }
});
</script>
