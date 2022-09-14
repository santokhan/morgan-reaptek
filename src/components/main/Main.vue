<script setup>
import Sidebar from "./sidebar/Sidebar.vue";
import Container from "./container/Container.vue";
import Details from "./details/Details.vue";
import SidebarMobile from "./sidebar-mobile/SidebarMobile.vue";
</script>
<script>
export default {
  props: ["status", "hideSidebar"],
  data() {
    return {
      navId: 0,
      cardId: null,
    };
  },
  methods: {
    sidebarHandler(n) {
      this.navId = n;
    },
    detailsHandler(cardId) {
      this.cardId = cardId;
    },
  },
};
</script>
<template>
  <div class="flex relative h-full">
    <Sidebar
      :sidebarHandler="sidebarHandler"
      :detailsHandler="detailsHandler"
    />
    <SidebarMobile
      :sidebarHandler="sidebarHandler"
      :detailsHandler="detailsHandler"
      :status="status"
      :hideSidebar="hideSidebar"
    />
    <div class="w-full z-0">
      <Container
        v-if="cardId === null"
        :navId="navId"
        :detailsHandler="detailsHandler"
      />
      <Details
        v-if="typeof cardId === 'number'"
        :navId="navId"
        :cardId="cardId"
        :detailsHandler="detailsHandler"
      ></Details>
    </div>
  </div>
</template>
