<template>
  <div>
    <div class="row">
      <div class="col-6 flex">
        <div class="container">
          <h1>Lorem ipsum dolor sit amet</h1>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim
            ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut
            aliquip ex ea commodo consequat
          </p>
          <div>
            <button class="button">Enviar</button>
            <button class="button1">Mas info</button>
          </div>
        </div>
      </div>
      <div class="col-6">
        <div class="plomo"></div>
      </div>
    </div>
  </div>
</template>
<style scoped>
@media screen and (max-width: 720px) {
  .col-6 {
    min-width: 100%
  }
  .flex {
    height: 50vh
  }
  .plomo {
    height: 50vh;
  }
}
@media screen and (min-width: 721px) {
  .plomo {
    height: 100vh;
  }
}
.plomo {
  background-color: grey;
  width: 100%;
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
.button:hover,
.button1:hover {
  opacity: 1;
}
h1,
p {
  pointer-events: auto;
}
.flex {
  display: flex;
  align-items: center;
}
</style>
