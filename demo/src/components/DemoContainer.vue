<template>
  <div class="link_container">
    <router-link class="link" to="/">В меню</router-link>
  </div>
  <div class="container">
    <button @click="decrement"> - </button>

        <span> Current value: {{ count }} </span>

        <button @click="increment"> + </button>
    <!-- <slot /> -->
  </div>
</template>

<script setup>
import { ref } from 'vue'

const count = ref(0)
/* Метод уменьшения значения */
const decrement = () => {
  count.value = count.value - 1
}

/* Метод увеличения значения */
const increment = () => {
  count.value = count.value + 1
}

</script>

<style lang="scss" scoped>
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 20rem;
}
.link {
  border-bottom: 1px solid #343838FF;
  color: #343838FF;
  padding-bottom: .25rem;
  text-decoration: none;
}
.link_container {
  margin-left: 2rem;
  margin-top: 2rem;
}
</style>
