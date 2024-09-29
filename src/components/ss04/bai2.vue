<template>
    <div>
      <p>Company: {{ check === false ? hu.company : ha.company }}</p>
      <p>Age: {{ check === false ? hu.age : ha.age }}</p>
      <button @click="handleChange">Change data</button>
    </div>
  </template>
  <script setup>
  import { ref } from "vue";

  const ha = ref({
    company: "Rikkei Academy",
    age: 2,
  });
  const hu = ref({
    company: "Rikkei Education",
    age: 1,
  });
  
  const check = ref(false);
  const handleChange = () => {
    check.value = !check.value;
  };
  </script>
  <style></style>