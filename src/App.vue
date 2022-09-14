<script setup>
import Main from "./components/main/Main.vue";
import Header from "./components/header/Header.vue";
</script>
<script>
export default {
  data() {
    return {
      status: true,
    };
  },
  methods: {
    hideSidebar() {
      this.status = this.status ? false : true;
    },
  },
};
</script>
<template>
  <Header :hideSidebar="hideSidebar"></Header>
  <Main :status="status" :hideSidebar="hideSidebar"></Main>
</template>
