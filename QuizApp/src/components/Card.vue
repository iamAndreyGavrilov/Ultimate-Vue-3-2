<script setup>

const props = defineProps({
  quiz: Object,
})

const {quiz} = props

</script>


<template>
  <div class="card">
    <img
        :src="quiz.img"
        alt="">
    <div class="card-text">
      <h2>{{ quiz.name }}</h2>
      <p>{{ quiz.questions.length }} questions</p>
    </div>
  </div>
</template>


<style scoped>

.card {
  width: 310px;
  overflow: hidden;
  border-radius: 15px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 1);
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