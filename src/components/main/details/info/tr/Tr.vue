<script>
export default {
  props: ["td1"],
};
</script>
<template>
  <tr class="border">
    <td class="p-2">{{ td1 }}</td>
    <td class="text-center">
      <i
        class="fa fa-check bg-blue-500 rounded-full text-white p-1 text-lg"
        aria-hidden="true"
      ></i>
    </td>
  </tr>
</template>
