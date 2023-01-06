<script setup>

</script>

<template>
  <div>
    <header>
      <h4>Question 1/3</h4>
      <div class="bar">
        <div class="completion"></div>
      </div>
    </header>
    <div>
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
    </div>
  </div>
</template>


<style scoped>
header {
  display: flex;
  align-items: center;
  margin-top: 20px;
}

header h4 {
  font-size: 30px;
}

.bar {
  width: 300px;
  height: 30px;
  background-color: #ccc;
  border-radius: 10px;
  margin-left: 20px;
}

.completion {
  width: 0%;
  height: 100%;
  background-color: #4caf50;
  border-radius: 10px;
}

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
}

.option-label {
  font-size: 30px;
  font-weight: bold;
  margin-right: 20px;
}

.option-value {
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 10px;
  width: 300px;
}
</style>