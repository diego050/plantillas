<template>
    <div class="background">
      <div class="container pad">
        <br />
        <h2 align="center" v-scrolls>EQUIPO</h2>
        <br />
        <Section title="EQUIPO CREATIVO">
          <p align="justify">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
          </p>
        </Section>
        <hr />
        <Section title="QUIENES SOMOS">
          <p align="justify">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
          </p>
        </Section>
        <br />
      </div>
    </div>
  </template>
  
  <style scoped>
  @media screen and (max-width: 499px) {
    .background {
      background: linear-gradient(rgba(0, 0, 0, 0.6), rgba(0, 0, 0, 0.6)),
      url("/imagenes-webp/equipo/ima1-cel.webp");
    }
  }
  @media screen and (min-width: 500px) {
    .background {
      background: linear-gradient(rgba(0, 0, 0, 0.6), rgba(0, 0, 0, 0.6)),
      url("/imagenes-webp/equipo/ima1.webp");
    }
  }
  @media screen and (min-width: 721px) and (max-width: 960px) {
    .pad {
      padding-right: 100px;
      padding-left: 100px;
    }
  }
  @media screen and (min-width: 961px) and (max-width: 1140px) {
    .pad {
      padding-right: 150px;
      padding-left: 150px;
    }
  }
  @media screen and (min-width: 1141px) {
    .pad {
      padding-right: 250px;
      padding-left: 250px;
    }
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
  .background {
    background-size: cover;
    background-position: center center;
  }
  h2,
  h3,
  p,
  hr {
    color: white;
  }
  </style>
  
  <script>
  export default {
    components: {
      Section: {
        props: ['title'],
        template: `
          <div>
            <h3 v-scrolls>{{ title }}</h3>
            <slot></slot>
            <br />
          </div>
        `
      }
    }
  }
  </script>
  