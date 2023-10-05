<template>
  <div class="mt-8 p-8">
    <div class="flex justify-between relative">
      <img
        :src="productSection.image"
        class="h-40 mb-8 transition-all ease-linear delay-800 hover:scale-125"
      />
      <figcaption
        class="absolute top-[15%] right-[20%] uppercase bg-blue-100 text-blue-950 py-3.5 px-8 text-xs rounded-3xl"
      >
        {{ productSection.category }}
      </figcaption>
    </div>
    <h4 class="font-bold text-2xl">{{ productSection.name }}</h4>
    <p class="text-gray-400 mb-6">{{ productSection.company }}</p>
    <p class="text-green-600 mb-8">₹ {{ productSection.price }}</p>
    <button
      class="no-underline max-w-screen-xl text-white bg-blue-950 py-3 px-4 rounded-md uppercase text-center cursor-pointer transition-all duration-300 hover: shadow-blue-800 hover:scale-95"
      @click="
        () => {
          addItem(productSection.id);
        }
      "
    >
      Add to Cart
    </button>
  </div>
</template>

<script>
import { mapMutations } from "vuex";
export default {
  props: ["productSection"],
  methods: {
    ...mapMutations(["addItem"]),
  },
};
</script>

<style scoped></style>
