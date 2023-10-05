<template>
  <nav class="flex justify-between bg-slate-100 p-8">
    <NuxtLink
      to="/"
      class="no-underline text-blue-950 font-bold transition-colors ease-linear duration-300 hover:text-blue-300"
      ><img
        src="../assets/images/logo.png"
        alt=""
        class="w-20 absolute left-16 top-4"
    /></NuxtLink>
    <NuxtLink
      to="/cart"
      class="no-underline text-blue-950 font-bold transition-colors ease-linear duration-300 hover:text-blue-300"
      >My Cart</NuxtLink
    >
  </nav>
</template>

<script>
export default {};
</script>

<style scoped></style>
