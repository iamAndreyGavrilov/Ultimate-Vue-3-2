<script setup>
import Question from "@/components/Question.vue";
import QuizHeader from "@/components/QuizHeader.vue";
import {useRoute} from "vue-router";
import {ref, watch, computed} from "vue";
import q from "@/data/quizes.json";

const route = useRoute();
const quizId = parseInt(route.params.id);
const quiz = q.find((q) => q.id === quizId);
const currentQuestionIndex = ref(0); //"questions" array index, from json file

const questionStatus = computed(() => {
  return `${currentQuestionIndex.value}/${quiz.questions.length}`;
});
const barWidth = computed(() => {
  return `${(currentQuestionIndex.value / quiz.questions.length) * 100}%`;
});

const nextQuestion = () => {
  if (currentQuestionIndex.value < quiz.questions.length) {
    currentQuestionIndex.value++;
  }
};

</script>

<template>
  <div>
    <QuizHeader :questionStatus="questionStatus" :barWidth="barWidth"/>
    <div>
      <Question :question="quiz.questions[currentQuestionIndex]"/>
    </div>
    <button @click="nextQuestion">Next Question</button>
  </div>
</template>


<style scoped>

</style>