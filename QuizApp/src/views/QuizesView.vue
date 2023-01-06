<script setup>
import q from '../data/quizes.json'
import {ref, watch} from 'vue'
import Card from '../components/Card.vue'

const quizes = ref(q)
const search = ref('')

watch(search, () => {
  quizes.value = q.filter(quiz => quiz.name.toLowerCase().includes(search.value.toLowerCase()))
})


</script>

<template>
  <div>
    <header>
      <h1>Quizes</h1>
      <input v-model.trim="search" type="text" placeholder="Search...">
    </header>
    <div class="options-container">
      <Card v-for="quiz in quizes" :key="quiz.id" :quiz="quiz"/>
    </div>
  </div>
</template>

<style scoped>

header {
  display: flex;
  align-items: center;
  padding: 20px 0;
}

header h1 {
  font-weight: bold;
  margin-right: 30px;
}

header input {
  padding: 5px;
  border: 1px solid #ccc;
  border-radius: 5px;
  outline: none;
}

.options-container {
  display: flex;
  flex-wrap: wrap;
  margin-top: 40px;
}
</style>