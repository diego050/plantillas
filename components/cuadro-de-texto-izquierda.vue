<template>
  <div style="position: relative">
    <br class="display" />
    <br />
    <div class="container index" v-scrolls>
      <div class="row">
        <div class="col-6 order1">
          <!--<picture v-for="image in images" :key="image.src">
              <source :srcset="image.srcset" class="imagen" media="(min-width: 500px)" alt="Alt text" loading="lazy" />
              <img :src="image.src" class="imagen" alt="Alt text" loading="lazy" />
            </picture>-->
          <div style="width: 100%; height: 200px; background-color: grey"></div>
          <br />
          <br />
          <div class="columns">
            <div
              style="width: 100%; height: 200px; background-color: grey"
            ></div>
            <div
              style="width: 100%; height: 200px; background-color: grey"
            ></div>
            <!--<picture v-for="columnImage in columnImages" :key="columnImage.src">
                <source :srcset="columnImage.srcset" class="imagen" media="(min-width: 500px)" alt="Alt text" loading="lazy" />
                <img :src="columnImage.src" class="imagen" alt="Alt text" loading="lazy" />
              </picture>-->
          </div>
        </div>
        <div class="texto col-6 order">
          <div>
            <h2>NUESTRO ENFOQUE</h2>
            <p align="justify">
              Nos enfocamos en crear espacios que reflejen la personalidad y
              estilo de nuestros clientes, un estilo propio. La renderización 3D
              te brinda la posibilidad de crear objetos únicos, personalizando
              cada creación. Trabajamos en estrecha colaboración para comprender
              tus necesidades y deseos, y luego desarrollamos soluciones
              creativas y funcionales. Te ayudamos a mejorar tu calidad de vida,
              mejorar tu estado de salud, tu estado de ánimo y darte seguridad.
            </p>
          </div>
        </div>
      </div>
    </div>
    <br />
  </div>
</template>

<style scoped>
@media screen and (max-width: 499px) {
  .order {
    order: 1;
  }
  .order1 {
    order: 2;
  }
  h2 {
    font-size: 28px;
  }
  p {
    font-size: 18px;
  }
  .col-6 {
    width: 98%;
    padding-left: 1%;
    padding-right: 1%;
  }
  .display {
    display: none;
  }
}
@media screen and (min-width: 500px) and (max-width: 720px) {
  .order {
    order: 1;
  }
  .order1 {
    order: 2;
  }
  h2 {
    font-size: 30px;
  }
  p {
    font-size: 20px;
  }
  .col-6 {
    width: 98%;
    padding-left: 1%;
    padding-right: 1%;
  }
}
@media screen and (min-width: 721px) and (max-width: 960px) {
  h2 {
    font-size: 25px;
  }
  p {
    font-size: 20px;
  }
  .col-6 {
    width: 48%;
    padding-left: 1%;
    padding-right: 1%;
  }
}
@media screen and (min-width: 961px) and (max-width: 1140px) {
  h2 {
    font-size: 30px;
  }
  p {
    font-size: 21px;
  }
  .col-6 {
    width: 48%;
    padding-left: 1%;
    padding-right: 1%;
  }
}
@media screen and (min-width: 1141px) {
  h2 {
    font-size: 33px;
  }
  p {
    font-size: 23px;
  }
  .col-6 {
    width: 48%;
    padding-left: 1%;
    padding-right: 1%;
  }
}
.columns {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  column-gap: 10px;
}
.index {
  z-index: 2;
  position: relative;
}
.texto {
  display: flex;
  align-items: center;
}
h2 {
  margin: 0;
}
.imagen {
  width: 100%;
  height: 200px;
  object-fit: cover;
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

<script>
export default {
  data() {
    return {
      images: [
        {
          srcset: "/imagenes-webp/texto-con-imagenes/ima1.webp",
          src: "/imagenes-webp/texto-con-imagenes/ima1-cel.webp",
        },
      ],
      columnImages: [
        {
          srcset: "/imagenes-webp/texto-con-imagenes/ima2.webp",
          src: "/imagenes-webp/texto-con-imagenes/ima2-cel.webp",
        },
        {
          srcset: "/imagenes-webp/texto-con-imagenes/ima3.webp",
          src: "/imagenes-webp/texto-con-imagenes/ima3-cel.webp",
        },
      ],
    };
  },
};
</script>
