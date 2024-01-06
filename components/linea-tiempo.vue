<template>
  <div v-scrolls style="position: relative">
    <br />
    <h2 align="center">Lorem ipsum dolor</h2>
    <br />
    <div class="timeline">
      <div v-for="(step, index) in steps" :key="index" :class="step.position">
        <span :class="step.spanClass">{{ step.number }}</span>
        <div class="content">
          <h3>{{ step.title }}</h3>
          <p align="justify">{{ step.description }}</p>
        </div>
      </div>
    </div>
    <div
      v-for="(circle, index) in circles"
      :key="index"
      :class="circle.class"
      :style="circle.style"
    ></div>
    <br />
  </div>
</template>

<style scoped>
.circulo {
  width: 50px;
  height: 50px;
  background-color: #e0e0e0;
  border-radius: 50%;
  position: absolute;
  z-index: 1;
}
.circulo1 {
  width: 50px;
  height: 50px;
  background-color: #cacaca;
  border-radius: 50%;
  position: absolute;
  z-index: 1;
}
h2 {
  font-size: 40px;
  margin-bottom: 0;
  z-index: 2;
  position: relative;
}
h3 {
  font-size: 22px;
  margin-bottom: 0;
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
* {
  box-sizing: border-box;
}
.timeline {
  position: relative;
  max-width: 1200px;
  margin: 0 auto;
}
.timeline::after {
  content: "";
  position: absolute;
  width: 6px;
  background-color: grey;
  top: 0;
  bottom: 0;
  left: 50%;
  margin-left: -3px;
}

/* Container around content */
.container1 {
  padding: 10px 40px;
  position: relative;
  background-color: inherit;
  width: 50%;
}
.container1::after {
  content: "";
  position: absolute;
  width: 25px;
  height: 25px;
  right: -17px;
  background-color: white;
  border: 4px solid grey;
  top: 15px;
  z-index: 1;
}
span {
  position: absolute;
  top: 23px;
  margin-left: -3px;
  z-index: 3;
  color: grey;
}
.spanle {
  left: 100%;
  transform: translateX(-10%);
}
.spanri {
  right: 100%;
  transform: translateX(60%);
}
.left {
  left: 0;
}

.right {
  left: 50%;
}
.left::before {
  content: " ";
  height: 0;
  position: absolute;
  top: 22px;
  width: 0;
  z-index: 1;
  right: 30px;
  border: medium solid #e0e0e0;
  border-width: 10px 0 10px 10px;
  border-color: transparent transparent transparent #e0e0e0;
}

/* Add arrows to the right container (pointing left) */
.right::before {
  content: " ";
  height: 0;
  position: absolute;
  top: 22px;
  width: 0;
  z-index: 1;
  left: 30px;
  border: medium solid #e0e0e0;
  border-width: 10px 10px 10px 0;
  border-color: transparent #e0e0e0 transparent transparent;
}
.right::after {
  left: -16px;
}

/* The actual content */
.content {
  padding: 20px 30px;
  background-color: #e0e0e0;
  position: relative;
  border-radius: 6px;
}

/* Media queries - Responsive timeline on screens less than 600px wide */
@media screen and (max-width: 600px) {
  .display {
    display: none;
  }
  .spanle {
    left: 31px;
  }
  .spanri {
    left: 28px;
  }

  /* Place the timelime to the left */
  .timeline::after {
    left: 31px;
  }

  /* Full-width containers */
  .container1 {
    width: 100%;
    padding-left: 70px;
    padding-right: 25px;
  }

  /* Make sure that all arrows are pointing leftwards */
  .container1::before {
    left: 60px;
    border: medium solid white;
    border-width: 10px 10px 10px 0;
    border-color: transparent white transparent transparent;
  }

  /* Make sure all circles are at the same spot */
  .left::after,
  .right::after {
    left: 15px;
  }

  /* Make all right containers behave like the left ones */
  .right {
    left: 0%;
  }
}
</style>

<script>
export default {
  data() {
    return {
      steps: [
        {
          number: 1,
          title: "Lorem ipsum dolor sit amet",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam.",
          position: "container1 left",
          spanClass: "spanle",
        },
        {
          number: 2,
          title: "Lorem ipsum dolor sit",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam.",
          position: "container1 right",
          spanClass: "spanri",
        },
        {
          number: 3,
          title: "Lorem ipsum dolor",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam.",
          position: "container1 left",
          spanClass: "spanle",
        },
      ],
      circles: [
        { class: "circulo", style: { top: "30px", left: "30px" } },
        { class: "circulo1", style: { top: "40px", left: "40px" } },
        { class: "circulo display", style: { bottom: "30px", left: "30px" } },
        { class: "circulo1 display", style: { bottom: "40px", left: "40px" } },
        { class: "circulo", style: { top: "30px", right: "30px" } },
        { class: "circulo1", style: { top: "40px", right: "40px" } },
        { class: "circulo display", style: { bottom: "30px", right: "30px" } },
        { class: "circulo1 display", style: { bottom: "40px", right: "40px" } },
      ],
    };
  },
};
</script>
