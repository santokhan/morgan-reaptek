<script setup>
import Toggler from "./toggler/Toggler.vue";
import Logo from "./logo/Logo.vue";
</script>
<script>
export default {
  props: ["hideSidebar"],
};
</script>
<template>
  <div class="app-header flex items-center px-1">
    <div class="flex items-center">
      <Toggler :hideSidebar="hideSidebar" />
      <Logo></Logo>
    </div>
  </div>
</template>
