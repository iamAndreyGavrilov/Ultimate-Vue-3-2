<script setup>
import {RouterLink} from "vue-router";

const {
  quizQuestionsLength,
  numberOfCorrectAnswers
} = defineProps(["quizQuestionsLength", "numberOfCorrectAnswers"]);

</script>

<template>
  <div class="results">
    <p>Results...</p>
    <h1>You got {{ numberOfCorrectAnswers }} / {{ quizQuestionsLength }} correct</h1>
    <RouterLink class="restart" to="/">Restart</RouterLink>
  </div>
</template>


<style scoped>
.results {
  text-align: center;
  padding: 100px 0;
}

p {
  font-size: 30px;
}

h1 {
  font-size: 100px;
  color: #777;
}

.restart {
  margin-top: 20px;
  font-size: 30px;
  color: black;
  text-decoration: none;
}

.restart:hover {
  text-decoration: underline;
}
</style>