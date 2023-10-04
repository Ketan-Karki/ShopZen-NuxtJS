<template>
  <div>
    <div class="cart_heading">
      <p>Item</p>
      <p>Price</p>
      <p>Quantity</p>
      <p>Subtotal</p>
      <p>Remove</p>
    </div>
    <hr />
    <div class="cart-item">
      <MyItem v-for="item in myCart" :key="item.id" :item="item" />
    </div>
  </div>
</template>

<script>
import { mapState } from "vuex";

export default {
  computed: {
    ...mapState(["myCart"]),
  },
};
</script>

<style>
.cart_heading {
  margin: 2em;
  text-align: center;
  text-transform: uppercase;
  display: grid;
  grid-template-columns: repeat(4, 1fr) 0.3fr;
  align-items: center;
}
hr {
  margin-top: 1rem;
}
</style>
