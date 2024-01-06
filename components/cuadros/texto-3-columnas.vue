<template>
  <div style="position: relative">
    <br class="display" />
    <br />
    <div class="container index" v-scrolls>
      <div class="row">
        <div class="col-4 width">
          <h1>Lorem ipsum dolor sit amet</h1>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim
            ad minim veniam,
          </p>
        </div>
        <div class="col-4 width1">
          <div>
            <h2>Lorem ipsum dolor sit amet</h2>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
              eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut
              enim ad minim veniam,
            </p>
          </div>
          <br />
          <div>
            <h2>Lorem ipsum dolor sit amet</h2>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
              eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut
              enim ad minim veniam,
            </p>
          </div>
          <br />
          <div>
            <h2>Lorem ipsum dolor sit amet</h2>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
              eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut
              enim ad minim veniam,
            </p>
          </div>
        </div>
        <div class="col-4 width1">
          <div>
            <h2>Lorem ipsum dolor sit amet</h2>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
              eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut
              enim ad minim veniam,
            </p>
          </div>
          <br />
          <div>
            <h2>Lorem ipsum dolor sit amet</h2>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
              eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut
              enim ad minim veniam,
            </p>
          </div>
          <br />
          <div>
            <h2>Lorem ipsum dolor sit amet</h2>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
              eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut
              enim ad minim veniam,
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
  h2 {
    font-size: 28px;
  }
  p {
    font-size: 18px;
  }
  .width,.width1 {
    min-width: 98%;
    padding-left: 1%;
    padding-right: 1%;
  }
}
@media screen and (min-width: 500px) and (max-width: 720px) {
  h2 {
    font-size: 30px;
  }
  p {
    font-size: 20px;
  }
  .width {
    min-width: 98%;
    padding-left: 1%;
    padding-right: 1%;
  }
  .width1 {
    min-width: 48%;
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
}
@media screen and (min-width: 961px) and (max-width: 1140px) {
  h2 {
    font-size: 30px;
  }
  p {
    font-size: 21px;
  }
}
@media screen and (min-width: 1141px) {
  h2 {
    font-size: 33px;
  }
  p {
    font-size: 23px;
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
