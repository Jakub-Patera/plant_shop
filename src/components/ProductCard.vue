<template>
    <div class="relative w-[350px]">
      <div class="flex justify-center items-center flex-col">
        <div class="relative">
          <div class="flex justify-center flex-col items-center">
            <div
              class="h-28 w-28 bg-[#e6efef] rounded-full absolute top-28 left-6 -mt-14 ml-16 z-10"
            ></div>
            <img :src="image" alt="Product" class="w-1/2 h-auto relative z-20 hover:bottom-3 hover:transition-all hover:duration-300" />
          </div>
          <div class="flex justify-start flex-col mt-2">
            <h2 class="pl-24 text-lg font-bold">{{ title }}</h2>
            <div class="flex flex-row justify-evenly">
              <p class="font-bold">{{ price }}</p>
              <button>Koupit</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      image: String,
      title: String,
      price: String,
    },
  };
  </script>