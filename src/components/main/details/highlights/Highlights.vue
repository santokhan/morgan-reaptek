<script setup>
import Card from "./card/Card.vue";
</script>
<template>
  <div class="p-2">
    <div class="bg-white rounded border">
      <div class="border-b px-2 sm:px-4">
        <div class="font-medium py-2">Highlights</div>
      </div>
      <div class="flex flex-wrap sm:p-2 overflow-y-auto info">
        <Card />
        <Card />
        <Card />
        <Card />
        <Card />
        <Card />
        <Card />
        <Card />
      </div>
    </div>
  </div>
</template>
