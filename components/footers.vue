<template>
  <div class="background">
    <br />
    <div class="container">
      <div class="columns">
        <div>
          <p>apartado 1</p>
          <p>apartado 2</p>
          <p>apartado 3</p>
        </div>
        <div>
          <p>apartado 1</p>
          <p>apartado 2</p>
          <p>apartado 3</p>
        </div>
        <div class="flex">
          <a href="/">
            <img src="" alt="logo de facebook" class="imagen" loading="lazy" />
          </a>
          <a href="/">
            <img src="" alt="logo de instagram" class="imagen" loading="lazy" />
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
@media screen and (max-width: 359px) {
  .flex {
    display: flex;
    gap: 20px;
    height: 100%;
  }
}
@media screen and (min-width: 360px) {
  .flex {
    display: flex;
    flex-direction: column;
    gap: 10px;
    align-items: flex-end;
    justify-content: center;
    height: 100%;
  }
  .columns {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    column-gap: 10px;
  }
}
h2 {
  margin-top: 0;
}
h2,
p {
  color: white;
}
.background {
  background-color: black;
}
.imagen {
  max-width: 45px;
  width: 100%;
  height: 100%;
  object-fit: contain;
  filter: invert(100%);
}
</style>
