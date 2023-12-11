<script setup>
import { ref } from 'vue';

const startAnimation = (element) => {
  const target = document.querySelector(`.${element}`);
  if (target) {
    target.style.transform = 'scale(1.1)';
  }
};

const stopAnimation = (element) => {
  const target = document.querySelector(`.${element}`);
  if (target) {
    target.style.transform = 'scale(1)';
  }
};
</script>

<template>
  <section class="container">
    <div class="left-section">
      <div class="row">
        <div class="House" @mouseover="startAnimation('House')" @mouseout="stopAnimation('House')">
          <p class="section-title">House</p>
        </div>
        <div class="Icarus" @mouseover="startAnimation('Icarus')" @mouseout="stopAnimation('Icarus')">
          <p class="section-title">Icarus</p>
        </div>
        <div class="castle" @mouseover="startAnimation('castle')" @mouseout="stopAnimation('castle')">
          <p class="section-title">Castle</p>
        </div>
      </div>
    </div>
    <div class="right-section">
      <div class="racoom3">
        <img src="https://drive.google.com/uc?export=view&id=1qeI6kL5awBvpozBxCm8ekDhA3iXVNA82" alt="" class="image" />
      </div>
    </div>
  </section>
</template>

<style scoped>
.container {
  display: flex;
  justify-content: space-between;
}

.left-section {
  display: flex;
  flex-direction: column;
}

.row {
  display: flex;
  gap: 20px;
}

.right-section {
  flex-shrink: 0;
}

.racoom3 {
  position: relative;
  background-color: red;
  height: 150px;
  width: 150px;
  border-radius: 30%;
  margin-top: 20px;
  transition: transform 0.3s ease; /* Agrega una transición a la propiedad transform */
}

.Icarus,
.House,
.castle {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 400px;
  width: 200px;
  background-color: red;
  border-radius: 20px;
  position: relative;
  overflow: hidden;
  transition: transform 0.3s ease; /* Agrega una transición a la propiedad transform */
}

.section-title {
  margin: 0;
  position: absolute;
  bottom: 0;
  left: 0;
  transform: translateY(100%);
  opacity: 0;
  transition: opacity 0.5s ease, transform 0.5s ease;
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
}

.row:hover .section-title {
  opacity: 1;
  transform: translateY(0);
}

.row:hover .House {
  transform: scale(1.1);
}

.row:hover .Icarus {
  transform: scale(1.1);
}

.row:hover .castle {
  transform: scale(1.1);
}

/* Agrega animación de desplazamiento a las letras */
.House:hover .section-title,
.Icarus:hover .section-title,
.castle:hover .section-title {
  opacity: 1;
  transform: translateY(0) translateX(-10px);
}

@media screen and (max-width: 600px) {
  .Icarus,
  .House,
  .castle {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 200px;
    width: 150px;
    background-color: red;
    border-radius: 20px;
    position: relative;
    overflow: hidden;
    transition: transform 0.3s ease; 
  }

  .racoom3 {
    position: relative;
    background-color: red;
    height: 150px;
    width: 150px;
    border-radius: 30%;
    margin-top: 20px;
    transition: transform 0.3s ease; 
    order: 24px; 
  }
}
</style>