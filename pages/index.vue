<template>
  <div class="container">
    <div class="grid grid-cols-3">
      <ProductDisplay
        v-for="productInfo in data"
        :key="productInfo.id"
        :productSection="productInfo"
      />
    </div>
  </div>
</template>

<script>
import { data } from "~/assets/data";
export default {
  data() {
    return {
      data,
    };
  },
};
</script>

<style></style>
