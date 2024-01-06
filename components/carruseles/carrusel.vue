<template>
  <div class="container">
    <h2 align="center" v-scrolls>Lorem ipsum</h2>
    <p align="center" v-scrolls>
      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
      tempor incididunt ut labore et dolore magna aliqua.
    </p>
    <br />
    <div class="columns">
      <div
        class="slider"
        v-for="slider in sliders"
        :key="slider.id"
        :class="slider.display"
      >
        <div class="slide-track">
          <div
            v-for="n in slider.images"
            :key="n.alt"
            style="position: relative"
            :class="slider.effectClass"
          >
            <!--<picture>
              <source :srcset="n.srcset" class="imagen" media="(min-width: 500px)" :alt="n.alt" />
              <img :src="n.ima" class="imagen" :alt="n.alt" />
            </picture>-->
            <div
              style="
                background-color: grey;
                height: 200px;
                width: 100%;
                object-fit: contain;
              "
            ></div>
          </div>
        </div>
      </div>
    </div>
    <br />
  </div>
</template>

<style scoped>
@media screen and (max-width: 499px) {
  .display1 {
    display: none;
  }
  .display2 {
    display: none;
  }
}
@media screen and (min-width: 500px) and (max-width: 720px) {
  .columns {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    column-gap: 10px;
  }
  .display2 {
    display: none;
  }
  .display3 {
    display: none;
  }
}
@media screen and (min-width: 721px) and (max-width: 960px) {
  .columns {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    column-gap: 10px;
  }
  .display2 {
    display: none;
  }

  .display3 {
    display: none;
  }
}
@media screen and (min-width: 961px) {
  .columns {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    column-gap: 10px;
  }
  .display1 {
    display: none;
  }

  .display3 {
    display: none;
  }
}
h2 {
  font-size: 40px;
  margin-bottom: 0;
}
.logo {
  padding-top: 10px;
  padding-right: 10px;
  position: absolute;
  top: 0;
  right: 0;
  width: 80px;
  object-fit: contain;
  z-index: 2;
}
.before-enter {
  opacity: 0;
  transform: translateX(100px);
  transition: all 1s ease-out;
}
.enter {
  opacity: 1;
  transform: translateX(0px);
}
.slider {
  width: 100%;
  height: 600px;
  margin: auto;
  overflow: hidden;
}
.slider .slide-track {
  display: flex;
  flex-direction: column;
  row-gap: 25px;
  width: 100%;
}
.imagen {
  width: 100%;
  height: 100%;
  object-fit: contain;
  object-position: right;
  z-index: 1;
}
.efect {
  animation: scroll-compu 30s linear infinite;
}
.efect1 {
  animation: scroll-tablet 30s linear infinite;
}
.efect2 {
  animation: scroll-cel 50s linear infinite;
}
.efect3 {
  animation: scroll-compu 35s linear infinite;
}
.efect4 {
  animation: scroll-tablet 35s linear infinite;
}
@keyframes scroll-compu {
  0% {
    transform: translateY(0);
  }
  100% {
    transform: translateY(calc(-115% * 7));
  }
}
@keyframes scroll-tablet {
  0% {
    transform: translateY(0);
  }
  100% {
    transform: translateY(calc(-94% * 12));
  }
}
@keyframes scroll-cel {
  0% {
    transform: translateY(0);
  }
  100% {
    transform: translateY(calc(-118% * 20));
  }
}
</style>

<script>
export default {
  data() {
    return {
      pantallaGrande: false,
      pantallaMediana: false,
    };
  },
  computed: {
    sliders() {
      const imagen1 = [
        {
          ima: "",
          alt: "",
          srcset: "",
        },
        {
          ima: "",
          alt: "",
          srcset: "",
        },
        {
          ima: "",
          alt: "",
          srcset: "",
        },
        {
          ima: "",
          alt: "",
          srcset: "",
        },
        {
          ima: "",
          alt: "",
          srcset: "",
        },
        {
          ima: "",
          alt: "",
          srcset: "",
        },
        {
          ima: "",
          alt: "",
          srcset: "",
        },
        {
          ima: "",
          alt: "",
          srcset: "",
        },
        {
          ima: "",
          alt: "",
          srcset: "",
        },
        {
          ima: "",
          alt: "",
          srcset: "",
        },
        {
          ima: "",
          alt: "",
          srcset: "",
        },
        {
          ima: "",
          alt: "",
          srcset: "",
        },
        {
          ima: "",
          alt: "",
          srcset: "",
        },
        {
          ima: "",
          alt: "",
          srcset: "",
        },
        {
          ima: "",
          alt: "",
          srcset: "",
        },
        {
          ima: "",
          alt: "",
          srcset: "",
        },
        {
          ima: "",
          alt: "",
          srcset: "",
        },
        {
          ima: "",
          alt: "",
          srcset: "",
        },
        {
          ima: "",
          alt: "",
          srcset: "",
        },
        {
          ima: "",
          alt: "",
          srcset: "",
        },
        {
          ima: "",
          alt: "",
          srcset: "",
        },
      ];
      return [
        {
          id: 1,
          images: imagen1.slice(0, 7).concat(imagen1.slice(0, 3)),
          effectClass: "efect",
          display: "display2",
        },
        {
          id: 2,
          images: imagen1.slice(0, 10).concat(imagen1.slice(0, 3)),
          effectClass: "efect1",
          display: "display1",
        },
        {
          id: 3,
          images: imagen1.concat(imagen1.slice(0, 5)),
          effectClass: "efect2",
          display: "display3",
        },
        {
          id: 4,
          images: imagen1.slice(7, 14).concat(imagen1.slice(7, 10)),
          effectClass: "efect3",
          display: "display2",
        },
        {
          id: 5,
          images: imagen1.slice(10).concat(imagen1.slice(10, 13)),
          effectClass: "efect4",
          display: "display1",
        },
        {
          id: 6,
          images: imagen1.slice(14).concat(imagen1.slice(14, 17)),
          effectClass: "efect",
          display: "display2",
        },
      ];
    },
  },
  methods: {
    actualizarPantalla() {
      const width = window.innerWidth;
      this.pantallaGrande = width > 960;
      this.pantallaMediana = width >= 499 && width < 960;
      console.log(this.pantallaMediana);
    },
  },
  mounted() {
    window.addEventListener("resize", this.actualizarPantalla);
    this.actualizarPantalla();
  },
  beforeUnmount() {
    window.removeEventListener("resize", this.actualizarPantalla);
  },
};
</script>
