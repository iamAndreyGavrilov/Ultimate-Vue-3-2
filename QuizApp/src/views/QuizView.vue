<script setup>
import Question from "@/components/Question.vue";
import QuizHeader from "@/components/QuizHeader.vue";
import {useRoute} from "vue-router";
import {ref} from "vue";
import quizes from "@/data/quizes.json";

const route = useRoute();

const quizId = parseInt(route.params.id);

const quiz = quizes.find((quiz) => quiz.id === quizId);

const currentQuestionIndex = ref(0); //"questions" array index, from json file

</script>

<template>
  <div>
    <QuizHeader/>
    <div>
      <Question :question="quiz.questions[currentQuestionIndex]"/>
    </div>
  </div>
</template>


<style scoped>

</style>