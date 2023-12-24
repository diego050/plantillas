<template>
    <div>
        <div class="columns">
            <div>
                <h2 align="center">
                    asdasdasd
                </h2>
                <div class="pad">
              <input
                class="input1"
                type="text"
                placeholder="Nombre"
                v-model="nombre"
                :class="{ 'red-border': !Vinput1 }"
                @blur="validate1"
                @input="validate1"
              />
              <input
                class="input1"
                type="email"
                placeholder="E-mail"
                aria-describedby="emailHelp"
                v-model="correo"
                :class="{ 'red-border': !Vinput2 }"
                @input="validate2"
                @blur="validate2"
              />
              <textarea
                class="textarea1"
                type="text"
                rows="6"
                placeholder="Mensaje"
                v-model="texto"
                :class="{ 'red-border1': !Vinput3 }"
                @blur="validate3"
                @input="validate3"
              ></textarea>
              <div align="center">
                <button
                  class="button1"
                  v-on:click="form"
                  :disabled="isButtonDisabled"
                  :class="{ cursor: !isButtonDisabled }"
                >
                  ENVIAR
                </button>
              </div>
              <br />
            </div>
            </div>
            <div class="background">
                <div class="container">
                <h3>
                    asdsad
                </h3>
                <p>
                    asdasdasd
                </p>
            </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  data() {
    return {
      nombre: "",
      correo: "",
      texto: "",
      alert: false,
      alert1: false,
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
        this.correo == "" ||
        this.nombre == "" ||
        this.texto == ""
      );
    },
  },
  methods: {
    async form() {
    },
    validate1() {
      if (this.nombre === "") {
        this.Vinput1 = false;
      } else {
        this.Vinput1 = true;
      }
    },
    validate2() {
      const emailPattern = /^[a-zA-Z0-9._-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,4}$/;
      this.Vinput2 = emailPattern.test(this.correo);
    },
    validate3() {
      if (this.texto === "") {
        this.Vinput3 = false;
      } else {
        this.Vinput3 = true;
      }
    },
  },
};
</script>

<style scoped>
.columns {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    column-gap: 10px;
}
.background {
    background-color: grey;
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
  z-index: 1;
  opacity: 0;
  transition: opacity 0.3s ease;
}
.alert-success1 {
  opacity: 1;
}
.alert-success2 {
  z-index: 3
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
.input1 {
  width: 100%;
  height: 40px;
  max-width: 100%;
  display: block;
  margin-bottom: 30px;
  margin-right: auto;
  margin-left: auto;
  border: 1px solid #a3a3a3;
}
.input1:focus {
  border: 1px solid #000000;
}
.textarea1 {
  width: 100%;
  display: block;
  border: 1px solid #a3a3a3;
  border-radius: 5px;
  resize: none;
  margin-bottom: 30px;
}
.button1 {
  max-width: 100%;
  width: 300px;
  height: 40px;
  background-color: black;
  color: white;
  border: none;
  border-radius: 5px;
  transition: background-color 0.5s ease;
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
input:focus {
  outline: none !important;
}
.cursor {
  cursor: pointer;
}
</style>