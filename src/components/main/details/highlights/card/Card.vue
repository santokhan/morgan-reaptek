<script setup>
import higtlights from "./highlights.png";
</script>
<script>
export default {
  data() {
    return {
      src: "/src/assets/image/highlights.png",
    };
  },
};
</script>
<template>
  <div class="w-full sm:w-1/2 p-2">
    <div class="flex items-center border p-3 rounded">
      <div class="w-1/3">
        <img :src="higtlights" alt="highlights" />
      </div>
      <div class="w-full pl-2">
        <div class="font-medium">20 Original Posts Per Month</div>
        <div class="text-gray-500">
          Our team will research and post 20 original posts per month online.
          Original content is always used and hashtags are researched for
          trends.
        </div>
      </div>
    </div>
  </div>
</template>
