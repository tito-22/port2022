<script setup></script>

<template>
  <section class="container">
    <div class="Dove"></div>
    <div class="Racom2"></div>
    <div class="Icarus"></div>
  </section>
</template>

<style scoped>
.container {
  position: relative;
  width: 100%;
  height: 100vh;
}

.Dove {
  width: 50px; 
  height: 50px;
  background-color: red;
  position: absolute;
}
.Icarus {
  width: 50px; 
  height: 50px;
  background-color: red;
  position: absolute;
}

.Racom2 {
  width: 100px; 
  height: 100px;
  background-color: red;
  position: absolute;
  border-radius: 20px;
}

.Dove {
  top: 0;
  right: 0;
}

.Racom2 {
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  
}

.Icarus {
  bottom: 0;
  left: 0;
}
</style>