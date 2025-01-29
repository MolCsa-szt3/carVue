<template>
  <h2>Add a car!</h2>

  <form @submit.prevent="save">
    <input type="text" v-model="brand" placeholder="Brand"><br>
    <input type="text" v-model="model" placeholder="Model"><br>
    <input type="number" v-model="year"><br>
    <button>Mentés</button>
  </form>
</template>

<style>
</style>
<script setup>
import axios from "axios";

import { onMounted, ref } from "vue";

const apiClient = axios.create({
  baseURL: "https://surveys-5jvt.onrender.com/api/cars/",
  headers: {
    "Content-Type": "application/json",
  },
});
const model = ref()
const brand = ref()
const year = ref(2000)
const save = ()=>{

}

</script>
