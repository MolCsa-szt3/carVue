<script setup>
import axios from "axios";

import { onMounted, ref } from "vue";

const apiClient = axios.create({
  baseURL: "https://surveys-5jvt.onrender.com/api/cars/",
  headers: {
    "Content-Type": "application/json",
  },
});

const getCars = async () => {
  apiClient
    .get("/")
    .then((response) => {
      cars.value = response.data;
    })
    .catch((error) => {
      console.error(error);
    });
};
const cars = ref([]);

onMounted(() => {
  getCars();
});
</script>

<template>
  <main>
    <h2>All them cars</h2>
    <div>
      <div v-for="car in cars" :key="car.id">
        <h5>{{ car.brand }} {{ car.model }}</h5>
      </div>
    </div>
  </main>
</template>
