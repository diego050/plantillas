<template>
  <div>
    <div class="container">
      <div class="row">
        <div class="col-6 width">
          <h1>Lorem ipsum dolor sit amet</h1>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim
            ad minim veniam,
          </p>
        </div>
        <div class="col-6">
            <div class="plomo"></div>
            <br />
        </div>
        <div class="col-3">
            <div style="padding-right: 15px;">
                <div style="height: 50px"></div>
                <div class="plomo"></div>
            </div>
        </div>
        <div class="col-5">
                <div class="plomo" style="height: 100%"></div>
        </div>
        <div class="col-4">
            <div style="padding-left: 15px;">
                <div class="plomo"></div>
            </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped>
@media screen and (max-width: 499px) {
    .width {
        min-width: 98%;
        padding-left: 1%;
        padding-right: 1%;
    }
}
@media screen and (min-width: 500px) and (max-width: 720px) {
    .width {
        min-width: 98%;
        padding-left: 1%;
        padding-right: 1%;
    }
    .col-5,.col-4,.col-3 {
        min-width: 50%
    }
}
@media screen and (min-width: 721px) and (max-width: 960px) {}
@media screen and (min-width: 961px) and (max-width: 1140px) {}
@media screen and (min-width: 1141px) {}
.plomo {
    width: 100%; 
    height: 200px; 
    background-color: grey;
    min-width: 100px;
}
</style>