<template>
  <div style="position: relative">
    <div style="background-color: #e0e0e0; position: relative">
      <div class="container">
        <br />
        <h2 class="texto" align="center">NUESTROS SERVICIOS</h2>
        <br />
        <div class="columns">
          <div
            v-for="service in data"
            :key="service.nombre"
            class="card"
            @click="showDialog(service)"
          >
            <!--<picture>
                <source
                  :srcset="service.srcset"
                  class="imagen"
                  media="(min-width: 500px)"
                  style="width: 100%; height: 250px; object-fit: cover"
                  :alt="service.alt"
                  loading="lazy"
                />
                <img
                  :src="service.ima"
                  style="width: 100%; height: 250px; object-fit: cover"
                  :alt="service.alt"
                  loading="lazy"
                />
              </picture>-->
            <div
              style="width: 100%; height: 200px; background-color: grey"
            ></div>
            <div class="container">
              <br />
              <h3 align="center" class="nomb">{{ service.nombre }}</h3>
              <p class="texto-limitado" align="justify">{{ service.info }}</p>
              <p align="center" style="color: grey">MÁS INFORMACIÓN</p>
              <br />
            </div>
            <div class="efect"></div>
          </div>
          <br />
        </div>
      </div>
    </div>
    <div v-for="service in data" :key="service.nombre">
      <Dibox v-show="service.show" @click="hideDialog(service)">
        <div>
          <div class="centro">
            <h3 class="nomb1">{{ service.nombre }}</h3>
            <button type="button" class="btn" @click="hideDialog(service)">
              X
            </button>
          </div>
          <br />
          <div>
            <p align="justify">
              {{ service.info }}
            </p>
          </div>
          <br />
        </div>
      </Dibox>
    </div>
  </div>
</template>

<style scoped>
@media screen and (min-width: 500px) and (max-width: 720px) {
  .columns {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    column-gap: 20px;
  }
}
@media screen and (min-width: 721px) and (max-width: 960px) {
  .columns {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    column-gap: 20px;
  }
}
@media screen and (min-width: 961px) and (max-width: 1140px) {
  .columns {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    column-gap: 20px;
  }
}
@media screen and (min-width: 1141px) {
  .columns {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    column-gap: 20px;
  }
}
h2 {
  font-size: 35px;
  margin: 0;
}
.btn {
  background-color: rgb(184, 0, 0);
  color: white;
  border: none;
  border-radius: 3px;
  font-size: 30px;
  height: 40px;
  cursor: pointer;
  transition: background-color 0.3s;
}
.btn:hover {
  background-color: red;
}
.card {
  background-color: #fff;
  border-radius: 4px;
  box-shadow: 0px 10px 20px rgba(0, 0, 0, 0.2);
  overflow: hidden;
  cursor: pointer;
  position: relative;
  z-index: 2;
  margin-bottom: 20px;
}
.centro {
  display: flex;
  justify-content: space-between;
  width: 100%;
  align-items: center;
}
.nomb {
  font-size: 23px;
  margin: 0;
}
.nomb1 {
  font-size: 30px;
  margin: 0;
}
.texto {
  z-index: 2;
  position: relative;
}
.texto-limitado {
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 3;
  -webkit-box-orient: vertical;
}
.efect {
  background-color: rgba(0, 0, 0, 1);
  opacity: 0;
  width: 100%;
  height: 100%;
  position: absolute;
  z-index: 2;
  top: 0;
  transition: opacity 0.3s;
}
.efect:hover {
  opacity: 0.1;
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
</style>

<script type="module" defer>
export default {
  data() {
    return {
      data: [
        {
          nombre: "",
          info: "",
          ima: "",
          srcset: "",
          show: false,
          alt: "",
        },
        {
          nombre: "",
          info: "",
          ima: "",
          srcset: "",
          show: false,
          alt: "",
        },
        {
          nombre: "",
          info: "",
          ima: "",
          srcset: "",
          show: false,
          alt: "",
        },
      ],
    };
  },
  unmounted() {
    document.body.style.position = "static";
    document.body.style.top = "";
    document.body.style.width = "";
    document.body.style.overflowY = "auto";
    window.scrollTo({ top: this.scrollPosition, behavior: "instant" });
  },
  methods: {
    showDialog(service) {
      this.scrollPosition = window.pageYOffset;
      service.show = true;
      console.log(this.scrollPosition);
      document.body.style.position = "fixed";
      document.body.style.top = `-${this.scrollPosition}px`;
      document.body.style.width = "100%";
      document.body.style.overflowY = "scroll";
    },
    hideDialog(service) {
      service.show = false;
      document.body.style.position = "static";
      document.body.style.top = "";
      document.body.style.width = "";
      document.body.style.overflowY = "";
      window.scrollTo({ top: this.scrollPosition, behavior: "instant" });
    },
  },
};
</script>
