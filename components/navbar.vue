<template>
  <div>
    <nav class="navbar" :class="{ navbar1: showBackground }">
      <div class="container">
        <div class="navbar-brand" @click="scrollTo('#parte1')" title="Página de inicio">
          <img src="" style="width: 60px; height: 100%; object-fit: cover" alt="Logo" loading="lazy" />
        </div>
        <ul class="navbar-nav">
          <li v-for="section in sections" :key="section.id" class="nav-item link1">
            <NuxtLink class="nav-link" :to="section.to" :class="{ 'nav-link1': showBackground }">
              {{ section.label }}
            </NuxtLink>
          </li>
          <li class="nav-item offcan">
            <div class="nav-link offcan">
              <LazyOffcanva />
            </div>
          </li>
        </ul>
      </div>
    </nav>
  </div>
</template>

<style scoped>
@media screen and (min-width: 1080px) {
  .nav-link.offcan {
    display: none;
  }
  .nav-item.offcan {
    display: none;
  }
}
@media screen and (max-width: 1081px) {
  .nav-link.link1 {
    display: none;
  }
  .nav-item.link1 {
    display: none;
  }
}
.input1 {
  padding: 8px;
  margin-right: 40px;
  width: 100%;
}
.navbar {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  padding-bottom: 12px;
  background-color: transparent;
  padding-top: 12px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  z-index: 999;
  transition: background-color 0.3s;
}

.navbar1 {
  background-color: white;
}

.container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.navbar-brand {
  font-size: 24px;
  font-weight: bold;
  color: #333333;
  text-decoration: none;
  padding-left: 2%;
}

.navbar-nav {
  display: flex;
  list-style: none;
  margin: 0;
  padding: 0;
}

.nav-item {
  margin-right: 15px;
  justify-content: center;
  display: flex;
  align-items: center;
  font-family: "Didact Gothic";
}

.nav-link {
  font-size: 20px;
  opacity: 0.7;
  color: white;
  text-decoration: none;
  font-family: "Didact Gothic";
  transition: opacity 0.3s;
}

.nav-link1 {
  color: #333333;
}
.nav-link.router-link-exact-active {
  opacity: 1;
}

.nav-link:hover {
  opacity: 1;
}
.invert {
  filter: invert(100%);
}
</style>

<script type="module" defer>
export default {
  data() {
    return {
      showBackground: false,
      sections: [
        { id: 1, label: 'Apartado 1', to: '/' },
        { id: 2, label: 'Apartado 2', to: '/', align: 'center' },
        { id: 3, label: 'Apartado 3', to: '/', align: 'center' },
        { id: 4, label: 'Apartado 4', to: '/' },
        { id: 5, label: 'Apartado 5', to: '/' },
        { id: 6, label: 'Apartado 6', to: '/' },
        { id: 7, label: 'Apartado 7', to: '/' },
      ],
    };
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll);
  },
  beforeDestroy() {
    window.removeEventListener('scroll', this.handleScroll);
  },
  methods: {
    handleScroll() {
      this.showBackground = window.pageYOffset > 20 || document.body.style.position === 'fixed';
    },
    scrollTo(nombre) {
      const targetElement = document.querySelector(nombre);
      const offset = 60;
      const targetPosition = targetElement.getBoundingClientRect().top + window.pageYOffset - offset;
      window.scrollTo({ top: targetPosition, behavior: 'smooth' });
    },
  },
};
</script>

