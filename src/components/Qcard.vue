<template>
    <div class="relative top-0 z-10">
      
        
            <h2 @click="toggleItem" :class="{'p-8 rounded-lg bg-[#3e6565] text-white': isOpen, 'p-8 rounded-lg bg-white flex justify-center order-2': !isOpen }">{{ title }}
                
                
            <p v-if="isOpen" class="pb-8 max-w-[300px] text-center">{{ answer }}</p>
            </h2>
        
      </div>
    
  </template>
  
  <script>
  import { ref } from 'vue';
  
  export default {
    props: {
      title: String,
      answer: String,
      isOpen: Boolean,
    },
    setup(props) {
      const isOpen = ref(props.isOpen);
  
      const toggleItem = () => {
        isOpen.value = !isOpen.value;
      };
  
      return {
        isOpen,
        toggleItem,
      };
    },
  };
  </script>