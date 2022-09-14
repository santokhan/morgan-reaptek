<script>
export default {
  props: [
    "sidebarHandler",
    "data",
    "id",
    "detailsHandler",
    "img",
    "hideSidebar",
    "handleSidebarStatusOnSelect",
  ],
  data() {
    return {};
  },
};
</script>
<template>
  <div
    class="bg-white border rounded-lg xl:rounded-xl p-2 m-2 hover:bg-blue-500 hover:text-white"
    title="Navigation Button"
    @click="
      () => {
        sidebarHandler(id);
        detailsHandler(null);
        handleSidebarStatusOnSelect();
      }
    "
  >
    <div class="flex items-center">
      <div class="px-1">
        <img class="rounded-lg w-14 xl:w-16" :src="img[id]" alt="sidebar" />
      </div>
      <div class="w-full xl:px-1">
        <div class="text-sm font-medium">{{ data.title }}</div>
        <div class="text-xs font-medium">{{ data.des }}</div>
        <div class="text-xs opacity-75 font-medium">
          Starting at ${{ data.price }}
        </div>
      </div>
      <div class="xl:px-1">
        <i class="fa fa-angle-right" aria-hidden="true"></i>
      </div>
    </div>
  </div>
</template>
