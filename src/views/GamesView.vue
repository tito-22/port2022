<script setup></script>

<template>
  <section class="container">
    <div class="left-section">
      <div class="castle">
        <p class="section-title">Castle</p>
      </div>
      <div class="GoRazer">
        <p class="section-title">GoRazer</p>
      </div>
    </div>
    <div class="right-section">
      <div class="racoom2">
        <img src="https://drive.google.com/uc?export=view&id=1qeI6kL5awBvpozBxCm8ekDhA3iXVNA82" alt="" class="image" />
      </div>
    </div>
  </section>
</template>

<style scoped>
.container {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
}

.left-section {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.right-section {
  overflow-y: auto;
}

.racoom2 {
  position: relative;
  background-color: rgba(97, 0, 255, 1);
  height: 150px;
  width: 150px;
  border-radius: 30%;
  top: 100px;
  left: 20px;
}

.GoRazer,
.castle {
  height: 200px;
  width: 500px;
  background-color: rgba(97, 0, 255, 1);
  border-radius: 20px;
  position: relative;
}

.section-title {
  position: absolute;
  color: white;
  font-size: 2rem;
  font-weight: bold;
  font-style: italic;
  right: 20px;
  bottom: 20px;
  transform: translateY(100%);
  opacity: 0;
  transition: opacity 0.5s ease, transform 0.5s ease;
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
}

.GoRazer:hover .section-title,
.castle:hover .section-title {
  transform: translateY(0%);
  opacity: 1;
}

@media screen and (max-width: 600px) {

  .GoRazer,
.castle {
  height: 100px;
  width: 240px;
  background-color: rgba(97, 0, 255, 1);
  border-radius: 20px;
  position: relative;
}
.racoom2 {
  position: relative;
  background-color: rgba(97, 0, 255, 1);
  height: 150px;
  width: 150px;
  border-radius: 30%;
  top: 100px;
  left: 20px;
}
}
</style>