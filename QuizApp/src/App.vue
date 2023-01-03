<script setup>
import q from './data/quizes.json'
import {ref} from 'vue'

const quizes = ref(q)

</script>

<template>
  <div class="container">
    <header>
      <h1>Quizes</h1>
      <input type="text" placeholder="Search...">
    </header>
    <div class="options-container">
      <div v-for="quiz in quizes" :key="quiz.id" class="card">
        <img
            :src="quiz.img"
            alt="">
        <div class="card-text">
          <h2>{{ quiz.name }}</h2>
          <p>{{ quiz.questions.length }} questions</p>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.container {
  max-width: 1000px;
  margin: 0 auto;
}

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

/* Card */

.card {
  width: 310px;
  overflow: hidden;
  border-radius: 2%;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
  margin: 10px;
  cursor: pointer;
}

.card img {
  width: 100%;
  height: 200px;
  object-fit: cover;
}

.card .card-text {
  padding: 10px;
}

.card .card-text h2 {
  font-weight: bold;
}
</style>