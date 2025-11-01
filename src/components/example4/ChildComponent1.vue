<!-- ChildComponent.vue -->
<template>
  <h3> Child 1 </h3>
  <div>
    <p>{{ sharedMessage }}</p>
  </div>

  <h3> Child 2 </h3>
  <div>
    <ChildComponent2 />
  </div>
</template>

<script setup>
import { inject } from 'vue';
import ChildComponent2 from "@/components/example4/ChildComponent2.vue";

// inject() 함수를 사용하여 상위 컴포넌트의 데이터를 주입받습니다.
const sharedMessage = inject('sharedMessage');
</script>

<style scoped>
p {
  color: red;
}
</style>