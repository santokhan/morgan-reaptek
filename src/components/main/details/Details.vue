<script setup>
import Overview from "./overview/Overview.vue";
import Info from "./info/Info.vue";
import Highlights from "./highlights/Highlights.vue";
import FAQ from "./faq/FAQ.vue";
import data from "./details.json";

import tiktok from "../../../assets/image/tiktok.png";
import social from "../../../assets/image/social.png";
import seo from "../../../assets/image/seo.png";
import google from "../../../assets/image/google.png";
import facebook from "../../../assets/image/facebook.png";
import content from "../../../assets/image/content.png";
import listing from "../../../assets/image/listing.png";
</script>
<script>
export default { props: ["navId", "cardId", "detailsHandler"] };
</script>
<template>
  <Overview
    :data="data[navId][cardId]"
    :detailsHandler="detailsHandler"
    :img="[tiktok, social, seo, google, facebook, content, listing]"
    :navId="navId"
  />
  <div class="flex flex-wrap">
    <div class="w-full xl:w-1/2"><Highlights /></div>
    <div class="w-full xl:w-1/2"><Info /></div>
  </div>
  <div class="w-full"><FAQ :data="data[navId][cardId].faq" /></div>
</template>
