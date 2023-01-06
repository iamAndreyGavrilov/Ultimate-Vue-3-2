<script setup>

</script>

<template>
  <div class="question-container">
    <h2 class="question">
      What is the capital of France?
    </h2>
  </div>
  <div class="options-container">
    <div class="option">
      <p class="option-label">A</p>
      <div class="option-value">
        <p>Paris</p>
      </div>
    </div>
    <div class="option">
      <p class="option-label">B</p>
      <div class="option-value">
        <p>Paris</p>
      </div>
    </div>
    <div class="option">
      <p class="option-label">C</p>
      <div class="option-value">
        <p>Paris</p>
      </div>
    </div>
    <div class="option">
      <p class="option-label">D</p>
      <div class="option-value">
        <p>Paris</p>
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