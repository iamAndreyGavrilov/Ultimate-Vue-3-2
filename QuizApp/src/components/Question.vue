<script setup>
const question = defineProps({
  question: Object,
})

const {text, options} = question.question

</script>

<template>
  <div class="question-container">
    <h2 class="question">
      {{ text }}
    </h2>
  </div>
  <div class="options-container">
    <div v-for="option in options" :key="option.id" class="option">
      <p class="option-label">{{ option.label }}</p>
      <div class="option-value">
        <p>{{ option.text }}</p>
      </div>
    </div>
  </div>
</template>


<style scoped>
.question-container {
  margin-top: 20px;
}

.question {
  font-size: 30px;
  font-weight: bold;
  margin-bottom: 20px;
}

.option {
  display: flex;
  align-items: center;
  margin-top: 20px;
  cursor: pointer;
  background-color: #cccccc;
}

.option-label {
  font-size: 30px;
  font-weight: bold;
  margin-right: 20px;
  background-color: #181818;
  color: white;
  width: 50px;
  height: 50px;
  text-align: center;
}

.option-value {
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 10px;
  width: 300px;
}
</style>