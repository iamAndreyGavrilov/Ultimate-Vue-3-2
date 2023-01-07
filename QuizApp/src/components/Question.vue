<script setup>
const {question} = defineProps(["question"]);

const emit = defineEmits(['selectOption'])

const emitSelectOption = (isCorrect) => {
  emit('selectOption', isCorrect)
}

</script>

<template>
  <div class="question-container">
    <h2 class="question">
      {{ question.text }}
    </h2>
  </div>
  <div class="options-container">
    <div v-for="option in question.options" :key="option.id" class="option" @click="emitSelectOption(option.isCorrect)">
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