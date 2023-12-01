<script setup></script>

<template>
  <section class="container">
    <div class="Dove"><h1>Dove</h1></div>
    <div class="Racom2"><img src="" alt=""></div>
    <div class="Icarus"><h2>Icarus</h2></div>
  </section>
</template>

<style scoped>
.container {
  position: relative;
  width: 100%;
  height: 100vh;
  margin: 20px;
}

.Dove {
  width: 700px; 
  height: 200px;
  background-color: rgba(255, 122, 0, 1);
  position: absolute;
  border-radius: 20px;
  top: 0;
  right: 30px;
}
.Icarus {
  width: 700px; 
  height: 200px;
  background-color: rgba(255, 122, 0, 1);
  position: absolute;
  border-radius: 20px;
  bottom: 0;
  left: 30px;
}


.Racom2 {
  width: 150px; 
  height: 150px;
  background-color: rgba(255, 122, 0, 1);
  position: absolute;
  border-radius: 20px;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

@media screen and (max-width: 600px) {

}

</style>