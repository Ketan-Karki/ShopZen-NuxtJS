<template>
  <div>
    <img :src="`${card.image}`" />
    <h3 class="header">
      {{ card.name }}
    </h3>
    <p class="snippet">
      {{ card.company }}
    </p>
  </div>
</template>

<script>
export default {
  props: ["card"],
};
</script>

<style scoped>
.header {
  font-size: 1.15rem;
  margin-top: 0.4rem;
  color: black;
}

.header:hover {
  color: black;
  text-decoration: none;
}
.snippet {
  color: grey;
}
</style>
