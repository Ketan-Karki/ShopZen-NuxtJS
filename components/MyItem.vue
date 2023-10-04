<template>
  <div>
    <div class="cart_heading">
      <div class="cart-image--name">
        <div>
          <figure>
            <img :src="item.image" alt="{id}" />
          </figure>
        </div>
        <div>
          <p>{{ item.name }}</p>
        </div>
      </div>
      <div>
        <p class="price">₹ {{ item.price }}</p>
      </div>
      <div>
        <div className="cart-button">
          <div className="amount-toggle">
            <button @click="() => setDecrease()">-</button>
            <div className="amount-style">{amount}</div>
            <button @click="() => setIncrease()">+</button>
          </div>
        </div>
      </div>
      <div><p>SubTotal</p></div>
      <div>
        <button
          class="button"
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

<style scoped>
.item-container {
  margin: 30px;
}
.text-container {
  padding: 0 10px;
}
img {
  /* width: 105px; */
  height: 200px;
  object-fit: cover;
}
p {
  font-size: 18px;
  color: grey;
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
}

.cart_heading {
  margin: 2em;
  text-align: center;
  text-transform: uppercase;
  display: grid;
  grid-template-columns: repeat(4, 1fr) 0.3fr;
  align-items: center;
}

.cart-image--name {
  /* background-color: red; */
  align-items: center;
  display: grid;
  gap: 1rem;
  grid-template-columns: 0.4fr 1fr;
  text-transform: capitalize;
  text-align: left;
}
.cart-image--name > img {
  max-width: 5rem;
  height: 5rem;
  object-fit: contain;
  color: transparent;
}
</style>
