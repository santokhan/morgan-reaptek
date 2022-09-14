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
  props: ["sidebarHandler", "detailsHandler"],
};
</script>
<template>
  <div class="sm:w-80 hidden sm:block">
    <div class="bg-gray-50 py-2 sm:py-0">
      <NavItem
        v-for="(item, i) in data"
        :data="item"
        :sidebarHandler="sidebarHandler"
        :id="i"
        :img="[tiktok, social, seo, google, facebook, content, listing]"
        :detailsHandler="detailsHandler"
      />
    </div>
  </div>
</template>
