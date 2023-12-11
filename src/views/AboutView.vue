<template>
  <section class="container">
    <div class="left-section">
      <img src="https://drive.google.com/uc?export=view&id=1qeI6kL5awBvpozBxCm8ekDhA3iXVNA82" alt="Mi Foto" class="profile-image" />
    </div>
    <div class="right-section">
      <h1>Gustavo Andres Rojas Tolosa</h1>
      <p></p>
    </div>
  </section>
</template>

<style scoped>
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

.left-section {
  flex-shrink: 0;
  margin-right: 20px;
}

.profile-image {
  width: 200px; 
  height: auto;
  border-radius: 50%;
}

.right-section {
  max-width: 600px; /* Ajusta el ancho máximo del texto según tus necesidades */
}

h1 {
  font-size: 2rem;
  margin-bottom: 10px;
  color: white;
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
}

p {
  font-size: 1.2rem;
  line-height: 1.5;
  color: aliceblue;
  font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
}
</style>