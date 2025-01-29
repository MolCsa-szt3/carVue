<script setup>
import { RouterLink, RouterView } from "vue-router";
</script>

<template>
  <header>
    <nav>
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/add">Add Car</RouterLink>
    </nav>
  </header>

  <RouterView />
</template>

<style scoped>
nav * {
  margin: 5px;
  border: 2px solid black;
  padding: 2px;
}
</style>
