<script setup>
import Tr from "./tr/Tr.vue";
</script>
<template>
  <div class="p-2">
    <div class="bg-white border rounded">
      <div class="py-2 px-2 sm:px-4 font-medium">Information</div>
      <hr />
      <div class="overflow-y-auto info pb-1">
        <div class="p-2 sm:p-4 text-gray-500">
          This plan includes 3 blog articles per month that are 500 words each.
          The blogs will be written out by one of our content experts and
          checked for quality by another expert. All blogs written by our team
          are 100% original and can help rank your clients' websites pages
          higher and attract more visitors.
        </div>
        <hr />
        <div class="py-2 px-2 sm:px-4">
          <table class="w-full">
            <thead class="font-medium">
              <td class="text-left" width="91%">Content Monthly</td>
              <td width="9%">Articles</td>
            </thead>
            <tbody class="text-gray-500">
              <Tr td1="Content Monthly"></Tr>
              <Tr td1="Content Monthly"></Tr>
              <Tr td1="Content Monthly"></Tr>
              <Tr td1="Content Monthly"></Tr>
              <Tr td1="Content Monthly"></Tr>
              <Tr td1="Content Monthly"></Tr>
              <Tr td1="Content Monthly"></Tr>
              <Tr td1="Content Monthly"></Tr>
              <Tr td1="Content Monthly"></Tr>
            </tbody>
          </table>
        </div>
      </div>
    </div>
  </div>
</template>
