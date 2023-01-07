<script setup>
import Question from "@/components/Question.vue";
import QuizHeader from "@/components/QuizHeader.vue";
import {useRoute} from "vue-router";
import {ref, watch, computed} from "vue";
import quizes from "@/data/quizes.json";

const route = useRoute();
const quizId = parseInt(route.params.id);
const quiz = quizes.find((quiz) => quiz.id === quizId);
const currentQuestionIndex = ref(0); //"questions" array index, from json file

const questionStatus = computed(() => {
  return `${currentQuestionIndex.value}/${quiz.questions.length}`;
});
const barWidth = computed(() => {
  return `${(currentQuestionIndex.value / quiz.questions.length) * 100}%`;
});

</script>

<template>
  <div>
    <QuizHeader :questionStatus="questionStatus" :barWidth="barWidth"/>
    <div>
      <Question :question="quiz.questions[currentQuestionIndex]"/>
    </div>
    <button @click="currentQuestionIndex++">Next Question</button>
  </div>
</template>


<style scoped>

</style>