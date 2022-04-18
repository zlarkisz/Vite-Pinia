<template>
  <div class="home">
    <h1>Home</h1>
    <Counter />

    <div class="buttons">
      <button @click="storeCounter.decreaseCount">-</button>
      <button @click="storeCounter.increaseCount">+</button>
    </div>
    <hr>
    <div>
      This counter is: {{ storeCounter.oddOrEvene }}
    </div>
    <hr>
    <div>
      <h3>Edit counter:</h3>
      <input
        v-model="storeCounter.count"
        type="number"
      >
    </div>
  </div>
</template>

<script setup>
import { useCounterStore } from '@/stores/counter'
import Counter from '@/components/Counter.vue'

const storeCounter = useCounterStore()
</script>


<style>
.count {
  font-size: 60px;
  margin: 20px;
}

.buttons button {
  font-size: 40px;
  margin: 10px;
}
</style>
