<template>
  <div>
    <div class="row">
      <div class="flex">
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
      <div class="flex1">
        <div class="column">
          <div style="height: 33vh"></div>
          <div class="plomo"></div>
        </div>

        <div class="column">
          <div style="height: 16.5vh"></div>
          <div class="plomo"></div>
          <div class="plomo"></div>
        </div>

        <div class="column">
          <div class="plomo"></div>
          <div class="plomo"></div>
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped>
@media screen and (max-width: 720px) {
  .flex {
    width: 100%;
  }
  .flex1 {
    width: 100%;
  }
}
@media screen and (min-width: 721px) {
  .bloque {
    background-color: transparent;
    height: 100px;
  }
  .flex {
    width: 600px;
  }
  .flex1 {
    flex: 1;
    position: relative;
  }
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
.flex1 {
  display: flex;
  justify-content: space-between;
  padding: 20px;
  overflow: hidden;
}
.flex {
  display: flex;
  align-items: center;
}

.column {
  flex: 1;
  margin: 0 5px;
  min-width: 200px;
}
.plomo {
  width: 100%;
  height: 33vh;
  margin-bottom: 10px;
  background-color: grey;
}
</style>
