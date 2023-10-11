<template>
  <div>
    <div class="mx-2 my-8 text-center uppercase grid grid-cols-5 items-center">
      <p class="col-span-1">Item</p>
      <p class="col-span-1">Price</p>
      <p class="col-span-1">Quantity</p>
      <p class="col-span-1">Subtotal</p>
      <p class="col-span-0.3">Remove</p>
    </div>
    <hr class="mt-1" />
    <div class="cart-item">
      <MyItem v-for="item in cartItems" :key="item.id" :item="item" />
    </div>
  </div>
</template>

<script>
import { mapGetters } from "vuex";

export default {
  computed: {
    ...mapGetters({
      cartItems: "getCartItems",
    }),
  },
  beforeMount() {
    this.$store.commit("INITIATE_CART");
  },
};
</script>

<style></style>
