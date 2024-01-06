<template>
  <div>
    <div style="position: relative">
      <swiper-container
        slides-per-view="1"
        speed="500"
        loop="true"
        autoplay-delay="2500"
        autoplay-disable-on-interaction="false"
      >
        <swiper-slide
          v-for="n in fondos"
          :style="{ 'background-color': n }"
        ></swiper-slide>
      </swiper-container>
      <div class="flex">
        <div class="container" align="center">
          <h1>Lorem ipsum dolor sit amet</h1>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim
            ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut
            aliquip ex ea commodo consequat
          </p>
          <div>
            <button class="button">Enviar</button>
            <button class="button1"> Mas info</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped>
swiper-container {
  height: 100vh;
  width: 100%;
  background-color: grey;
  position: relative;
  z-index: 1;
}
swiper-slide {
  background-color: grey;
}
.flex {
  position: absolute;
  display: flex;
  justify-content: center;
  align-items: center;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 2;
  width: 50%;
  pointer-events: none;
}
.button {
  width: 200px;
  height: 40px;
  color: white;
  background-color: black;
  border-radius: 8px;
  border: none;
  cursor: pointer;
  opacity: 0.7;
  pointer-events: auto;
  transition: opacity 0.3s ease-in-out;
  margin-right: 10px;
}
.button1 {
  width: 200px;
  height: 40px;
  color: black;
  background-color: transparent;
  border: none;
  cursor: pointer;
  opacity: 0.7;
  pointer-events: auto;
}
.button:hover, .button1:hover {
  opacity: 1
}
h1, p {
  pointer-events: auto;
}
</style>
<script setup>
useHead({
  script: [
    {
      src: "https://cdn.jsdelivr.net/npm/swiper@11/swiper-element-bundle.min.js",
    },
  ],
});
</script>
<script>
export default {
  data() {
    return {
      fondos: ["red", "blue", "grey"],
    };
  },
};
</script>
