<template>
  <div class="container">
    <div class="cards-container">
      <img :src="productSection.image" class="image" />
      <figcaption class="caption">{{ productSection.category }}</figcaption>
    </div>
    <h4 class="header">{{ productSection.name }}</h4>
    <p class="snippet">{{ productSection.company }}</p>
    <p class="price">₹ {{ productSection.price }}</p>
    <button
      class="button"
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

<style scoped>
.container {
  margin-top: 2rem;
  padding: 2rem;
}
.header {
  font-weight: 700;
  font-size: 1.5rem;
}
.snippet {
  color: grey;
  margin-bottom: 1.5rem;
}
.cards-container {
  display: flex;
  justify-content: space-between;
  position: relative;
}
.image {
  height: 165px;
  margin-bottom: 2em;
  transition: all 0.2s linear;
}

.image:hover {
  transform: scale(1.2);
}

.button {
  text-decoration: none;
  max-width: auto;
  color: white;
  background-color: rgb(28, 52, 84);
  padding: 0.75rem 1rem;
  border: none;
  border-radius: 5px;
  text-transform: uppercase;
  text-align: center;
  cursor: pointer;
  transition: all 0.3s ease;
  -webkit-transition: all 0.3s ease 0s;
  -moz-transition: all 0.3s ease 0s;
  -o-transition: all 0.3s ease 0s;
}

.button:hover {
  box-shadow: 0 2rem 2rem 0 rgb(132 144 255 / 30%);
  transform: scale(0.96);
}
.price {
  color: green;
  margin-bottom: 2em;
}

.caption {
  position: absolute;
  top: 15%;
  right: 20%;
  text-transform: uppercase;
  background-color: rgb(231, 242, 255);
  color: rgb(33, 37, 41);
  padding: 0.8rem 2rem;
  font-size: 12px;
  border-radius: 2rem;
}
</style>
