<!-- Carousel.vue -->
<template>
    <div class="container">
        <h2 align="center"> asdas as </h2>
        <br />
        <div class="columns">
  <div class="slider">
        <div class="slide-track">
            <div v-for="n in 7" class="slide">
                <!----<img :src="imagen1" alt="">-->
                <div style="background-color: grey; height: 200px"></div>
            </div>
        </div>
    </div>
    <div class="slider">
        <div class="slide-track">
            <div v-for="n in 7" class="slide">
                <!----<img :src="imagen1" alt="">-->
                <div style="background-color: grey; height: 200px"></div>
            </div>
        </div>
    </div>
    <div class="slider">
        <div class="slide-track">
            <div v-for="n in 7" class="slide">
                <!----<img :src="imagen1" alt="">-->
                <div style="background-color: grey; height: 200px"></div>
            </div>
        </div>
    </div>
</div>
<br />
</div>
</template>


<style scoped>
.columns {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    column-gap: 10px;
}
.slider {
    width: auto;
    height: 25vw;
    margin: auto;
    overflow: hidden;
}

.slider .slide-track {
    display: flex;
    flex-direction:column;
    row-gap: 25px;
    animation: scroll 40s linear infinite;
    -webkit-animation: scroll 40s linear infinite;
    height: calc(200px * 14);
}

.slider .slide {
    width: 200px;
}

.slider .slide img {
    width: 100%;
}

@keyframes scroll {
    0% {
        -webkit-transform: translateY(0);
        transform: translateY(0);
    }
    100% {
        -webkit-transform: translateY(calc(-200px * 7));
        transform: translateY(calc(-200px * 7));
    }
}
</style>

<script>
export default {
  data() {
    return {
      imagen1 : ""
    }
  }
}
</script>