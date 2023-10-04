<template>
  <div class="container">
    <div class="prodDisplay">
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

<style>
nav {
  display: flex;
  justify-content: space-between;
  background-color: whitesmoke;
  padding: 2em;
}

.navlinks {
  text-decoration: none;
  color: #35495e;
  font-weight: bold;
}

.prodDisplay {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
}
</style>
