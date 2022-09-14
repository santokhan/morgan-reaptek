<script setup>
import tiktok from "../../../../assets/image/tiktok.png";
import social from "../../../../assets/image/social.png";
import seo from "../../../../assets/image/seo.png";
import google from "../../../../assets/image/google.png";
import facebook from "../../../../assets/image/facebook.png";
import content from "../../../../assets/image/content.png";
import listing from "../../../../assets/image/listing.png";
</script>
<script>
export default {
  props: ["data", "detailsHandler", "img", "navId"],
  data() {
    return {
      src: "/src/assets/image/" + this.data.src + ".png",
    };
  },
};
</script>
<template>
  <div class="p-2">
    <div class="bg-white rounded border">
      <div class="p-2 sm:px-4 sm:pt-4">
        <button
          @click="detailsHandler(null)"
          class="text-blue-500 border border-blue-400 py-2 px-4 rounded-lg font-medium hover:bg-blue-600 hover:text-white focus:outline focus:outline-4 outline-blue-200"
          type="button"
        >
          Back to plans
        </button>
      </div>
      <div
        class="flex flex-col justify-center items-center max-w-7xl mx-auto pb-4"
      >
        <div>
          <img width="88" :src="img[navId]" alt="card" />
        </div>
        <div class="font-medium my-3 text-xl sm:text-2xl">{{ data.title }}</div>
        <div class="text-gray-500 text-center">{{ data.des }}</div>
        <div class="font-medium text-gray-500 my-2 text-center">
          ${{ data.price }}.00/month + $0.00/setup
        </div>
        <div class="text-gray-500 text-center">Compare plans</div>
      </div>
    </div>
  </div>
</template>
