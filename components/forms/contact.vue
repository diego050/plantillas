<template>
  <div class="background">
    <div v-if="alert" class="alert-success">Se envió correctamente</div>
    <br />
    <h2 align="center" v-scrolls>Lorem ipsum</h2>
    <div class="pad">
      <div class="row">
        <div class="col-8">
          <div class="container" v-scrolls>
            <h3>Lorem ipsum dolor</h3>
            <p align="justify">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
              eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut
              enim ad minim veniam, quis nostrud exercitation ullamco laboris
              nisi ut aliquip ex ea commodo consequat
            </p>
          </div>
        </div>
        <div class="col-4">
          <div class="container cuadro" v-scrolls>
            <br />
            <input
              v-model="nombre"
              :class="{ 'red-border': !Vinput1 }"
              @blur="validate1"
              @input="validate1"
              class="input1"
              type="text"
              placeholder="Nombre"
            />
            <input
              v-model="correo"
              :class="{ 'red-border': !Vinput2 }"
              @input="validate2"
              @blur="validate2"
              class="input1"
              type="email"
              placeholder="E-mail"
              aria-describedby="emailHelp"
            />
            <textarea
              v-model="texto"
              :class="{ 'red-border1': !Vinput3 }"
              @blur="validate3"
              @input="validate3"
              class="textarea1"
              rows="6"
              placeholder="Mensaje"
            ></textarea>
            <div align="center">
              <button
                v-on:click="form"
                :disabled="isButtonDisabled"
                :class="{ cursor: !isButtonDisabled }"
                class="button1"
              >
                ENVIAR
              </button>
            </div>
            <br />
          </div>
        </div>
      </div>
      <br />
      <br />
    </div>
  </div>
</template>

<style scoped>
@media screen and (max-width: 499px) {
  .col-4,
  .col-8 {
    width: 98%;
  }
  .background {
    background-color: grey;
  }
}
@media screen and (min-width: 500px) {
  .background {
    background-color: grey;
  }
}
@media screen and (min-width: 500px) and (max-width: 720px) {
  .col-4,
  .col-8 {
    width: 98%;
  }
}
@media screen and (min-width: 721px) and (max-width: 960px) {
  .col-4 {
    width: 39.66%;
  }
  .col-8 {
    width: 56.33%;
  }
}
@media screen and (min-width: 961px) and (max-width: 1140px) {
  .col-4 {
    width: 39.66%;
  }
  .col-8 {
    width: 56.33%;
  }
}
@media screen and (min-width: 1141px) {
  .col-4 {
    width: 39.66%;
  }
  .col-8 {
    width: 56.33%;
  }
  .pad {
    padding-right: 100px;
    padding-left: 100px;
  }
}
h2 {
  font-size: 40px;
}
h3 {
  margin-top: 0;
  font-size: 25px;
}
p {
  font-size: 18px;
}
.col-4 {
  padding-left: 1%;
  padding-right: 1%;
}
.col-8 {
  padding-left: 1%;
  padding-right: 1%;
}
h2,
h3,
p {
  color: white;
}
.alert-success {
  top: 20px;
  right: 2%;
  background-color: #d4edda;
  border-color: #c3e6cb;
  color: #155724;
  padding: 15px;
  border-radius: 4px;
  font-size: 16px;
  font-weight: bold;
  position: fixed;
  max-width: 100%;
  z-index: 5;
  opacity: 0;
  transition: opacity 0.3s ease;
  font-family: Arial, Helvetica, sans-serif;
}
.alert-success1 {
  opacity: 1;
}
.alert-success2 {
  z-index: 3;
}
.input1 {
  width: 90%;
  height: 40px;
  max-width: 100%;
  display: block;
  margin-bottom: 30px;
  margin-right: auto;
  margin-left: auto;
  border: 1px solid black;
  background-color: transparent;
}
.textarea1 {
  width: 90%;
  display: block;
  border-radius: 5px;
  resize: none;
  margin-right: auto;
  margin-left: auto;
  margin-bottom: 30px;
  background-color: transparent;
  border: 1px solid black;
}
.button1 {
  max-width: 90%;
  width: 300px;
  height: 40px;
  background-color: black;
  border: none;
  border-radius: 5px;
  transition: background-color 0.5s ease;
  color: white;
}
.button1:disabled {
  background-color: rgba(0, 0, 0, 0.795);
  color: rgba(255, 255, 255, 0.788);
}
.red-border {
  border: 1px solid red;
}
.red-border1 {
  border: 1px solid red;
}
.cursor {
  cursor: pointer;
}
.cuadro {
  background-color: rgba(255, 255, 255, 0.6);
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
//import axios from "axios";

export default {
  data() {
    return {
      nombre: "",
      correo: "",
      texto: "",
      alert: false,
      Vinput1: true,
      Vinput2: true,
      Vinput3: true,
    };
  },
  computed: {
    isButtonDisabled() {
      return (
        !this.Vinput1 ||
        !this.Vinput2 ||
        !this.Vinput3 ||
        this.correo === "" ||
        this.nombre === "" ||
        this.texto === ""
      );
    },
  },
  methods: {
    async form() {
      try {
        let result = await axios.post("", {
          correo: this.correo,
          nombre: this.nombre,
          texto: this.texto,
        });

        if (result.data.success) {
          this.alert = true;
          setTimeout(() => {
            this.alert = false;
          }, 5000);
          this.nombre = "";
          this.correo = "";
          this.texto = "";
        }
      } catch (error) {
        console.error(error);
      }
    },
    validate1() {
      this.Vinput1 = this.nombre !== "";
    },
    validate2() {
      const emailPattern = /^[a-zA-Z0-9._-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,4}$/;
      this.Vinput2 = emailPattern.test(this.correo);
    },
    validate3() {
      this.Vinput3 = this.texto !== "";
    },
  },
};
</script>
