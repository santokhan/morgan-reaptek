<script setup>
import Card from "./card/Card.vue";
import data from "./card.json";
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
  props: ["navId", "detailsHandler"],
};
</script>
<template>
  <div class="flex flex-wrap">
    <Card
      v-for="(item, i) in data[navId]"
      :data="item"
      :i="i"
      :img="[tiktok, social, seo, google, facebook, content, listing]"
      :navId="navId"
      :detailsHandler="detailsHandler"
    />
  </div>
</template>
