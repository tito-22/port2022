<script setup></script>

<template>
  <section class="container">
    <a href="https://drive.google.com/file/d/1zTSrckYThINEBxzoZV_2vVBlrvp3dIvU/view?t=12" target="_blank" class="Dove">
      <h1 class="section-title">Dove</h1>
    </a>
    <div class="racoom2">
      <img src="https://drive.google.com/uc?export=view&id=1qeI6kL5awBvpozBxCm8ekDhA3iXVNA82" alt="" class="image" />
    </div>
    <a href="https://drive.google.com/file/d/1I5OpHeChE9FxSJs3l0dSHxqqwZNrWcEi/view?t=2" target="_blank" class="Icarus">
      <h2 class="section-title">Icarus</h2>
    </a>
  </section>
</template>

<style scoped>
.container {
  position: relative;
  width: 100%;
  height: 100vh;
  margin: 20px;
}

.Dove,
.Icarus {
  width: 700px;
  height: 200px;
  background-color: rgba(255, 122, 0, 1);
  position: absolute;
  border-radius: 20px;
}

.Dove {
  top: 0;
  right: 30px;
}

.Icarus {
  bottom: 0;
  left: 30px;
}

.racoom2 {
  width: 150px;
  height: 150px;
  background-color: rgba(255, 122, 0, 1);
  position: absolute;
  border-radius: 20px;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
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

.Dove:hover .section-title,
.Icarus:hover .section-title {
  transform: translateY(0%);
  opacity: 1;
}

@media screen and (max-width: 600px) {

  .Dove,
.Icarus {
  width: 400px;
  height: 200px;
  background-color: rgba(255, 122, 0, 1);
  position: absolute;
  border-radius: 20px;
}

}
</style>