<template>
  <div class="h-2/3 flex justify-center items-center space-y-12 py-12 bg-[#3e6565]/30 flex-col">
    <h1 class="text-3xl font-bold">Most frequent questions?</h1>
    <div class="grid grid-cols-1  md:grid-cols-2 gap-4">
      <Qcard
        v-for="(item, index) in faqItems"
        :key="index"
        :title="item.title"
        :answer="item.answer"
        :isOpen="item.open"
        @toggle="toggleItem(index)"
      />
    </div>
  </div>
</template>

<script>
import Qcard from './Qcard.vue';

export default {
  components: {
    Qcard,
  },
  data() {
    return {
      faqItems: [
        {
          title: "My flowers are falling off or dying?",
          answer: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, voluptatum.",
          open: false,
        },
        {
          title: "What causes leaves to become pale?",
          answer: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, voluptatum.",
          open: false,
        },
        {
          title: "What causes brown crispy leaves?",
          answer: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, voluptatum.",
          open: false,
        },
        {
          title: "How do I choose a plant?",
          answer: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, voluptatum.",
          open: false,
        },
        {
          title: "How do I change the pots?",
          answer: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, voluptatum.",
          open: false,
        },
        {
          title: "Why are gnats flying around my plant?",
          answer: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, voluptatum.",
          open: false,
        },
        // Další položky FAQ
      ],
    };
  },
  methods: {
    toggleItem(index) {
      // Zavřít všechny karty kromě té, která byla právě otevřena
      this.faqItems.forEach((item, i) => {
        if (i !== index) {
          item.open = false;
        }
      });

      // Otevřít nebo zavřít kartu
      
      this.faqItems[index].open = !this.faqItems[index].open;
      
    },
  },
};
</script>
