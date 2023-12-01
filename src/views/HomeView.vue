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
        <a href="https://www.youtube.com/channel/UC5pu18O7t82cRI_Oky52mJQ" target="_blank" rel="noopener noreferrer">
          <img src="https://drive.google.com/uc?export=view&id=1UrBJ_MNShqUgMBBBj3hCwwje7psA5Zb7" alt="">
        </a>
         <a href="https://www.facebook.com/titoandres.rojastolosa" target="_blank" rel="noopener noreferrer">
           <img src="https://drive.google.com/uc?export=view&id=1Tqk2MbUsZUGXRgBklf80x3m6yBiiDCgE" alt="">
        </a>
         <a href="https://twitter.com/?lang=es" target="_blank" rel="noopener noreferrer">
           <img src="https://drive.google.com/uc?export=view&id=1kKFdAPyX9_zKUtTuZGFcVe7MUA3qhnLN" alt="">
        </a>
        <a href="https://www.twitch.tv/" target="_blank" rel="noopener noreferrer">
           <img src="https://drive.google.com/uc?export=view&id=19l7Z00jUH-Ei2i_Tr-2ph6Uy60AdMQ_c" alt="">
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
  border-radius: 20px;

}

.ANIMATION {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 700px;
  width: 300px;
  background-color: rgba(255, 122, 0, 1);
  border-radius: 20px;
}

.GAMES {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 700px;
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
  width: 70px; 
  height: 60px;
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

@media screen and (max-width: 1300px){

 .firstpage {
  display: flex;
  gap: 50px;
  opacity: 0;
  transform: translateY(50px);
  transition: opacity 1s ease, transform 1s ease;
}
  .Tresd {
   height: 700px;
  width: 270px;
  }
  .ANIMATION {
    height: 700px;
  width: 270px;
  }
  .GAMES {
   height: 700px;
  width: 270px;
  }
}
@media screen and (max-width: 900px){

 .firstpage {
  display: flex;
  gap: 30px;
  opacity: 0;
  transform: translateY(50px);
  transition: opacity 1s ease, transform 1s ease;
}
.Tresd {
   height: 700px;
  width: 250px;
  }
  .ANIMATION {
    height: 700px;
  width: 250px;
  }
  .GAMES {
   height: 700px;
  width: 250px;
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

