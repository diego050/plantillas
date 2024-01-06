<template>
  <div>
    <div v-for="(faq, index) in faqs" :key="index">
      <h2 @click="toggleAnswer(index)">
        {{ faq.question }}
      </h2>
      <p v-if="faq.showAnswer">
        {{ faq.answer }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      faqs: [
        {
          question: "What is Vue 3?",
          answer: "Vue 3 is the latest version of the Vue.js framework.",
          showAnswer: false,
        },
        {
          question: "What are the new features in Vue 3?",
          answer:
            "Vue 3 introduces several new features, including the Composition API, Fragments, Teleport, and more.",
          showAnswer: false,
        },
        {
          question: "How do I install Vue 3?",
          answer: "You can install Vue 3 using npm or yarn.",
          showAnswer: false,
        },
      ],
    };
  },
  methods: {
    toggleAnswer(index) {
      this.faqs[index].showAnswer = !this.faqs[index].showAnswer;
    },
  },
};
</script>
