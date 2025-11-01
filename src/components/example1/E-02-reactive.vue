<template>
  <div>{{ fullName }}</div>
</template>

<script setup>
import { ref, computed, onMounted } from 'vue';

const firstName = ref('Minho');
const lastName = ref('Park');

const fullName = computed(() => {
  return firstName.value + " " + lastName.value;
});

onMounted(() => {
  console.log('mounted');

  let a = 10;

  setTimeout(() => {
    console.log('setTimeout');
    a = 20;
    console.log(a);
  }, 500);

  setTimeout(() => {
    firstName.value = "123";
  }, 1000);

  setTimeout(() => {
    firstName.value = "PMH";
  }, 2000);
});
</script>