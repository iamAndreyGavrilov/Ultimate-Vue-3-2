<template>
  <div class="container">
    <header>
      <h1>Quizes</h1>
      <input type="text" placeholder="Search...">
    </header>
    <div class="options-container">
      <div class="card">
        <img
            src="https://imageio.forbes.com/specials-images/imageserve/62b1f965f3af80b3847a1f0b/Kids-who-seem-to-be-struggling-with-math-may-actually-be-struggling-with-language-/960x0.jpg?format=jpg&width=960"
            alt="Math">
        <div class="card-text">
          <h2>Math</h2>
          <p>15 questions</p>
        </div>
      </div>
      <div class="card">
        <img
            src="https://imageio.forbes.com/specials-images/imageserve/62b1f965f3af80b3847a1f0b/Kids-who-seem-to-be-struggling-with-math-may-actually-be-struggling-with-language-/960x0.jpg?format=jpg&width=960"
            alt="Math">
        <div class="card-text">
          <h2>Math</h2>
          <p>15 questions</p>
        </div>
      </div>
      <div class="card">
        <img
            src="https://imageio.forbes.com/specials-images/imageserve/62b1f965f3af80b3847a1f0b/Kids-who-seem-to-be-struggling-with-math-may-actually-be-struggling-with-language-/960x0.jpg?format=jpg&width=960"
            alt="Math">
        <div class="card-text">
          <h2>Math</h2>
          <p>15 questions</p>
        </div>
      </div>
      <div class="card">
        <img
            src="https://imageio.forbes.com/specials-images/imageserve/62b1f965f3af80b3847a1f0b/Kids-who-seem-to-be-struggling-with-math-may-actually-be-struggling-with-language-/960x0.jpg?format=jpg&width=960"
            alt="Math">
        <div class="card-text">
          <h2>Math</h2>
          <p>15 questions</p>
        </div>
      </div>
      <div class="card">
        <img
            src="https://imageio.forbes.com/specials-images/imageserve/62b1f965f3af80b3847a1f0b/Kids-who-seem-to-be-struggling-with-math-may-actually-be-struggling-with-language-/960x0.jpg?format=jpg&width=960"
            alt="Math">
        <div class="card-text">
          <h2>Math</h2>
          <p>15 questions</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>

</script>

<style scoped>
.container {
  max-width: 1000px;
  margin: 0 auto;
}

header {
  display: flex;
  align-items: center;
  padding: 20px 0;
}

header h1 {
  font-weight: bold;
  margin-right: 30px;
}

header input {
  padding: 5px;
  border: 1px solid #ccc;
  border-radius: 5px;
  outline: none;
}

.options-container {
  /*display: grid;*/
  /*grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));*/
  /*grid-gap: 20px;*/

  display: flex;
  flex-wrap: wrap;
  margin-top: 40px;
}

/* Card */

.card {
  width: 310px;
  overflow: hidden;
  border-radius: 2%;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
  margin: 10px;
  cursor: pointer;
}

.card img {
  width: 100%;
  height: 200px;
  object-fit: cover;
}

.card .card-text {
  padding: 10px;
}

.card .card-text h2 {
  font-weight: bold;
}
</style>