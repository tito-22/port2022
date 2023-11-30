<script setup>
import { ref, onMounted } from "vue";

const pageLoaded = ref(false);

onMounted(() => {
  // Simulamos la carga de la página después de 1 segundo (ajusta según sea necesario)
  setTimeout(() => {
    pageLoaded.value = true;
  }, 1000);
});
</script>

<template>
  <div>
    <div class="firstpage" :class="{ 'page-loaded': pageLoaded }">
      <div class="Tresd neon-box"><p>3D</p></div>
      <div class="ANIMATION neon-box"><p>ANIMATION</p></div>
      <div class="GAMES neon-box"><p>GAMES</p></div>
    </div>
    <div class="racoom neon-box" :class="{ 'page-loaded': pageLoaded }"></div>
  </div>
   <footer>
      <div class="social-icons">
        <a href="enlace_a_red_social" target="_blank" rel="noopener noreferrer">
          <!-- Puedes sustituir 'tu_icono_1.png' con la ruta de tu imagen -->
          <img src="./" alt="">
        </a>
         <a href="enlace_a_red_social" target="_blank" rel="noopener noreferrer">
          <!-- Puedes sustituir 'tu_icono_1.png' con la ruta de tu imagen -->
          <img src="tu_icono_1.png" alt="">
        </a>
       <a href="enlace_a_red_social" target="_blank" rel="noopener noreferrer">
          <!-- Puedes sustituir 'tu_icono_1.png' con la ruta de tu imagen -->
          <img src="tu_icono_1.png" alt="">
        </a>
        <a href="enlace_a_red_social" target="_blank" rel="noopener noreferrer">
          <!-- Puedes sustituir 'tu_icono_1.png' con la ruta de tu imagen -->
          <img src="tu_icono_1.png" alt="">
        </a>
      </div>
    </footer>
</template>

<style>
.racoom {
  position: absolute;
  top: 1%;
  left: 50%;
  transform: translateX(-50%);
  background-color: white;
  height: 150px;
  width: 150px;
  border-radius: 50%;
}

.firstpage {
  display: flex;
  gap: 60px;
  opacity: 0;
  transform: translateY(50px);
  transition: opacity 1s ease, transform 1s ease;
}

.firstpage.page-loaded {
  opacity: 1;
  transform: translateY(0);
}

.Tresd {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 700px;
  width: 300px;
  background-color: red;
  margin: 5px;
}

.ANIMATION {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 700px;
  width: 300px;
  background-color: rgba(255, 122, 0, 1);
  margin: 5px;
}

.GAMES {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 700px;
  width: 300px;
  background-color: rgba(97, 0, 255, 1);
  margin: 5px;
}

footer {
  background-color: black; 
  padding: 20px;
  text-align: center;
  gap: 20px;
}

.social-icons {
  display: flex;
  justify-content: center;
  gap: 10px;
}

.social-icons a {
  text-decoration: none;
  color: white; /* Color del icono de la red social */
}

.social-icons img {
  width: 30px; /* Tamaño del icono, ajusta según sea necesario */
  height: 30px;
}

.neon-box {
  box-shadow: 0 0 10px transparent, 0 0 20px transparent, 0 0 30px transparent,
    0 0 40px transparent, 0 0 50px transparent, 0 0 60px transparent,
    0 0 70px transparent;
  transition: box-shadow 0.3s ease;
}

.neon-box:hover {
  box-shadow: 0 0 10px red, 0 0 20px red, 0 0 30px red, 0 0 40px red,
    0 0 50px red, 0 0 60px red, 0 0 70px red;
}

.GAMES.neon-box:hover {
  box-shadow: 0 0 10px rgba(97, 0, 255, 1), 0 0 20px rgba(97, 0, 255, 1),
    0 0 30px rgba(97, 0, 255, 1), 0 0 40px rgba(97, 0, 255, 1),
    0 0 50px rgba(97, 0, 255, 1), 0 0 60px rgba(97, 0, 255, 1),
    0 0 70px rgba(97, 0, 255, 1);
}

.ANIMATION.neon-box:hover {
  box-shadow: 0 0 10px rgba(255, 122, 0, 1), 0 0 20px rgba(255, 122, 0, 1),
    0 0 30px rgba(255, 122, 0, 1), 0 0 40px rgba(255, 122, 0, 1),
    0 0 50px rgba(255, 122, 0, 1), 0 0 60px rgba(255, 122, 0, 1),
    0 0 70px rgba(255, 122, 0, 1);
}

@media screen and (max-width: 500px) {
  .firstpage {
    flex-direction: column;
    gap: 0px;
  }
  .Tresd {
    height: 200px;
    width: 500px;
  }
  .ANIMATION {
    height: 200px;
    width: 500px;
  }
  .GAMES {
    height: 200px;
    width: 500px;
  }
  .racoom {
    position: absolute;
    top: 90%;
    left: 95%;
    transform: translate(-50%, -50%);
    background-color: white;
    height: 150px;
    width: 150px;
    border-radius: 50%;
  }
}
</style>
