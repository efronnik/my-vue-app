<script setup>
import { ref} from 'vue';

const count = ref(0)
const name = ref('')
const isVisible = ref(true)

</script>

<template>
  <button @click="count++">Счетчик: {{ count }}</button>
  <button @click="count = 0"> Сбросить</button>
  <p v-if="count === 0">Ещё не кликали</p>
  <p v-else>Кликнули {{ count }} раз</p>
  <input v-model="name" placeholder="Введите имя" />
  <p>{{ name === '' ? 'Введите имя' : 'Привет, ' + name }}</p>
  <button @click="isVisible = !isVisible">Показать / скрыть</button>
  <p v-if="isVisible">Секретный текст</p>
</template>

<style scoped>
</style>
