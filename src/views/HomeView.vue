<script setup>
import { ref, onMounted } from "vue";
import { useRouter } from "vue-router"

const router = useRouter()

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
      <div class="Tresd neon-box" @click="router.push({ name: '3d' })">
        <p class="section-title">3D</p>
      </div>
      <div class="ANIMATION neon-box" @click="router.push({ name: 'animation' })">
        <p class="section-title">ANIMATION</p>
      </div>
      <div class="GAMES neon-box" @click="router.push({ name: 'games' })">
        <p class="section-title">GAMES</p>
      </div>
    </div>
    <div class="racoom neon-box" :class="{ 'page-loaded': pageLoaded }">
      <img src="https://drive.google.com/uc?export=view&id=1oBZUqEABdAdScCmxf5oJHKSs7TklZE1T" alt="" class="image" />
    </div>
  </div>
  <footer>
    <div class="social-icons">
      <a href="https://www.youtube.com/channel/UC5pu18O7t82cRI_Oky52mJQ" target="_blank" rel="noopener noreferrer">
        <img src="https://drive.google.com/uc?export=view&id=1FwDtWxUkjPepiPwR-EUSKw36efnHWfC5" alt="">
      </a>
      <a href="https://www.facebook.com/titoandres.rojastolosa" target="_blank" rel="noopener noreferrer">
        <img src="https://drive.google.com/uc?export=view&id=1ASCMNumaCP2gf479jOsnjm27TdI42cNF" alt="">
      </a>
      <a href="https://twitter.com/?lang=es" target="_blank" rel="noopener noreferrer">
        <img src="https://drive.google.com/uc?export=view&id=1cqiLGd4YE_q8KkXdBvvKOHYak1A0Hh_K" alt="">
      </a>
      <a href="https://www.twitch.tv/eltitovard" target="_blank" rel="noopener noreferrer">
        <img src="https://drive.google.com/uc?export=view&id=1YeYuVWLtz1vWGfnEUyJ7VyIaQgw61hka" alt="">
      </a>
      <a href="https://www.instagram.com/titowhat34/" target="_blank" rel="noopener noreferrer">
        <img src="https://drive.google.com/uc?export=view&id=1u470uez0zxgO9eldiD69J_YLI_yaZkZA" alt="">
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

.image {
  width: 70%;
  height: auto;
  left: 20px;
  top: 15px;
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
  height: 500px;
  width: 300px;
  background-color: red;
  border-radius: 20px;

}

.ANIMATION {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 500px;
  width: 300px;
  background-color: rgba(255, 122, 0, 1);
  border-radius: 20px;
}

.GAMES {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 500px;
  width: 300px;
  background-color: rgba(97, 0, 255, 1);
  border-radius: 20px;
}

footer {
  text-align: end;

}

.social-icons {
  display: flex;
  gap: 40px;
}

.social-icons img {
  width: 90%;
  height: 40px;
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

.racoom.neon-box:hover {
  box-shadow: 0 0 10px rgb(255, 255, 255), 0 0 20px rgb(255, 255, 255), 0 0 30px rgb(255, 255, 255), 0 0 40px rgb(255, 255, 255),
    0 0 50px rgb(255, 255, 255), 0 0 60px rgb(255, 255, 255), 0 0 70px rgb(254, 254, 254);
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

.section-title {
  position: absolute;
  color: white;
  font-size: 2rem;
  font-weight: bold;
  font-style: lazar;
  right: 20px;
  bottom: 20px;
  transform: translateX(100%) rotate(-90deg);
  transform-origin: 0% 100%;
}

@media screen and (max-width: 1300px) {

  .firstpage {
    display: flex;
    gap: 50px;
    opacity: 0;
    transform: translateY(50px);
    transition: opacity 1s ease, transform 1s ease;
  }

  .Tresd {
    height: 500px;
    width: 270px;
  }

  .ANIMATION {
    height: 500px;
    width: 270px;
  }

  .GAMES {
    height: 500px;
    width: 270px;
  }
}

@media screen and (max-width: 900px) {

  .firstpage {
    display: flex;
    gap: 30px;
    opacity: 0;
    transform: translateY(50px);
    transition: opacity 1s ease, transform 1s ease;
  }

}

@media screen and (max-width: 600px) {
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
    left: 86%;
    transform: translate(-50%, -50%);
    background-color: white;
    height: 150px;
    width: 150px;
    border-radius: 50%;
  }
}
</style>

