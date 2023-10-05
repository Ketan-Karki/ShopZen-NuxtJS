<template>
  <div>
    <div class="m-2 text-center uppercase grid grid-cols-5 items-center">
      <div
        class="col-span-1 items-center grid gap-1 grid-cols-2 capitalize text-left"
      >
        <div class="col-span-0.4">
          <figure>
            <img
              :src="item.image"
              alt="{id}"
              class="max-w-[5rem] h-20 object-contain"
            />
          </figure>
        </div>
        <div class="col-span-1">
          <p class="text-lg text-gray-600">{{ item.name }}</p>
        </div>
      </div>
      <div class="col-span-1">
        <p class="text-lg text-green-600">₹ {{ item.price }}</p>
      </div>
      <div class="col-span-1">
        <div className="cart-button">
          <div className="amount-toggle">
            <button @click="() => setDecrease()">-</button>
            <div className="amount-style">{amount}</div>
            <button @click="() => setIncrease()">+</button>
          </div>
        </div>
      </div>
      <div class="col-span-1">
        <p class="text-lg text-gray-600">SubTotal</p>
      </div>
      <div class="col-span-0.3">
        <button
          class="no-underline max-w-screen-xl text-white bg-blue-950 py-3 px-4 rounded-md uppercase text-center cursor-pointer transition-all duration-300 hover: shadow-blue-800 hover:scale-95"
          @click="
            () => {
              removeItem(item.id);
            }
          "
        >
          Remove
        </button>
      </div>
    </div>
    <hr />
  </div>
</template>

<script>
import { mapMutations } from "vuex";

export default {
  props: ["item"],
  methods: {
    ...mapMutations(["removeItem"]),
  },
};
</script>

<style scoped></style>
