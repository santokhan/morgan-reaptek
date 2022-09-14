<script>
export default {
  props: ["data", "i", "openFAQ", "FAQHandler"],
  data() {
    return {
      status: "hidden",
      rotate: "",
    };
  },
  methods: {
    handleShowHide() {
      this.status = this.status ? "" : "hidden";
      this.rotate = this.rotate ? "" : "rotate-90";
    },
  },
};
</script>
<template>
  <div class="border rounded my-2">
    <div class="font-medium p-3" @click="handleShowHide()">
      <i :class="rotate" class="fa fa-angle-right text-lg"></i>
      <span class="px-2">{{ data.q }}</span>
    </div>
    <div :class="status" class="py-2 px-4 border-t text-gray-500">
      {{ data.a }}
    </div>
  </div>
</template>
