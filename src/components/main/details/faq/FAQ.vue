<script setup>
import QA from "./qa/QA.vue";
</script>
<script>
export default {
  props: ["data"],
  data() {
    return {
      openFAQ: null,
    };
  },
  methods: {
    FAQHandler(n) {
      this.openFAQ = n;
    },
  },
};
</script>
<template>
  <div class="p-2">
    <div class="bg-white border rounded">
      <div class="font-medium py-2 px-2 sm:px-4 border-b">FAQ</div>
      <div class="sm:py-2 px-2 sm:px-4 h-80 overflow-y-auto">
        <QA
          v-for="(item, i) in data"
          :data="item"
          :i="i"
          :openFAQ="openFAQ"
          :FAQHandler="FAQHandler"
        ></QA>
      </div>
    </div>
  </div>
</template>
