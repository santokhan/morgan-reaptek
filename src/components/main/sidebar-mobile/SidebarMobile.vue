<script setup>
import NavItem from "./nav/NavItem.vue";
import data from "./sidebar.json";
import tiktok from "../../../assets/image/tiktok.png";
import social from "../../../assets/image/social.png";
import seo from "../../../assets/image/seo.png";
import google from "../../../assets/image/google.png";
import facebook from "../../../assets/image/facebook.png";
import content from "../../../assets/image/content.png";
import listing from "../../../assets/image/listing.png";
</script>
<script>
export default {
  props: ["sidebarHandler", "detailsHandler", "status", "hideSidebar"],
};
</script>
<template>
  <div
    v-if="status"
    class="w-full h-screen z-10 block sm:hidden absolute left-0 right-0 top-0 bottom-0 bg-gray-50"
    title="sidebar desktop"
  >
    <div class="bg-gray-50 py-2 sm:py-0">
      <NavItem
        v-for="(item, i) in data"
        :data="item"
        :sidebarHandler="sidebarHandler"
        :id="i"
        :img="[tiktok, social, seo, google, facebook, content, listing]"
        :detailsHandler="detailsHandler"
        :hideSidebar="hideSidebar"
      />
    </div>
  </div>
</template>
