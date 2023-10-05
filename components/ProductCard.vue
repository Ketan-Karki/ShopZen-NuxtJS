<template>
  <div>
    <img :src="`${card.image}`" />
    <h3 class="text-xl mt-1 text-black">
      {{ card.name }}
    </h3>
    <p class="text-gray-400">
      {{ card.company }}
    </p>
  </div>
</template>

<script>
export default {
  props: ["card"],
};
</script>

<style scoped></style>
