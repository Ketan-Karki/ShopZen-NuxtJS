<template>
  <nav>
    <NuxtLink to="/" class="navlinks"
      ><img src="../assets/images/logo.png" alt=""
    /></NuxtLink>
    <NuxtLink to="/cart" class="navlinks">My Cart</NuxtLink>
  </nav>
</template>

<script>
export default {};
</script>

<style scoped>
nav {
  display: flex;
  justify-content: space-between;
  background-color: rgb(231, 242, 255);
  padding: 2em;
}

.navlinks {
  text-decoration: none;
  color: rgb(33, 37, 41);
  font-weight: bold;
  transition: color 0.3s linear;
}

.navlinks:hover {
  color: rgb(110, 175, 255);
}

img {
  width: 78px;
  position: absolute;
  left: 4rem;
  top: 1rem;
}
</style>
