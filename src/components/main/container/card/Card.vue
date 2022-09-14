<script setup></script>
<script>
export default {
  props: ["data", "i", "detailsHandler", "img", "navId"],
};
</script>
<template>
  <div class="w-full xl:w-1/2 p-2">
    <div class="rounded-xl p-2 sm:px-3 bg-white border">
      <div class="flex items-center">
        <div>
          <img width="72" :src="img[navId]" alt="navigation-card" />
        </div>
        <div class="w-full flex justify-between items-center">
          <div class="px-2 py-1">
            <div class="text-base sm:text-lg font-medium">
              <button
                @click="detailsHandler(i)"
                class="text-blue-600 hover:text-blue-600"
                type="button"
              >
                {{ data.title }}
              </button>
            </div>
            <div class="font-medium text-gray-800">{{ data.subscription }}</div>
            <div class="text-sm sm:text-base opacity-75 font-medium">
              $199.00/monthly + ${{ data.price }}.00/setup
            </div>
          </div>
          <div class="sm:px-1 flex flex-col justify-center text-center">
            <a
              href="#"
              class="border border-blue-500 py-1 sm:py-2 px-2 sm:px-3 rounded-md text-blue-500 hover:text-white font-medium my-2 hover:bg-blue-500 focus:outline focus:outline-4 outline-blue-200"
              title="buy"
            >
              Buy <span class="hidden sm:inline">Now</span>
            </a>

            <button
              @click="detailsHandler(i)"
              class="text-blue-600 hover:underline block text-sm"
              type="button"
            >
              <span class="hidden sm:inline">Learn</span> more
            </button>
          </div>
        </div>
      </div>
      <p class="pt-1 sm:p-2 text-justify text-gray-500">{{ data.des }}</p>
    </div>
  </div>
</template>
