<script setup></script>
<script>
export default {
  props: ["hideSidebar"],
};
</script>
<template>
  <div>
    <button
      @click="hideSidebar()"
      type="button"
      class="px-2 block sm:hidden text-xl"
    >
      <i class="fa fa-bars" aria-hidden="true"></i>
    </button>
  </div>
</template>
