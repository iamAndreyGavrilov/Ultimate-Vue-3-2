<script setup>
import Question from "@/components/Question.vue";
import QuizHeader from "@/components/QuizHeader.vue";
import Result from "@/components/Result.vue";
import {useRoute} from "vue-router";
import {ref, watch, computed} from "vue";
import quizes from "@/data/quizes.json";

const route = useRoute();
const quizId = parseInt(route.params.id);
const quiz = quizes.find((quiz) => quiz.id === quizId);
const currentQuestionIndex = ref(0); //"questions" array index, from json file
const numberOfCorrectAnswers = ref(0);
const showResult = ref(false);

const questionStatus = computed(() => {
  return `${currentQuestionIndex.value}/${quiz.questions.length}`;
});
const barWidth = computed(() => {
  return `${(currentQuestionIndex.value / quiz.questions.length) * 100}%`;
});

const nextQuestion = () => {
  currentQuestionIndex.value++;
};

const onOptionSelected = (isCorrect) => {
  if (isCorrect) {
    numberOfCorrectAnswers.value++;
  }

  if (quiz.questions.length - 1 === currentQuestionIndex.value) {
    showResult.value = true;
  }

  nextQuestion();
};

</script>

<template>
  <div>
    <QuizHeader :questionStatus="questionStatus" :barWidth="barWidth"/>
    <div>
      <Question v-if="!showResult" :question="quiz.questions[currentQuestionIndex]" @selectOption="onOptionSelected"/>
      <Result :quizQuestionsLength="quiz.questions.length" :numberOfCorrectAnswers="numberOfCorrectAnswers" v-else/>
    </div>
  </div>
</template>


<style scoped>

</style>