<script setup>

const props = defineProps({
  questionStatus: String,
  barWidth: String,
})

</script>

<template>
  <header>
    <h4>Question {{ questionStatus }}</h4>
    <div class="bar">
      <div class="completion" :style="{width:barWidth}"></div>
    </div>
  </header>
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
</style>