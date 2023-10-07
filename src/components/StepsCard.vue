<template>
    <div class=" w-72 md:w-60 h-52 rounded-2xl bg-white justify-start items-start flex flex-col space-y-3 px-3 pt-6">
      <div class="w-12 h-14 bg-[#3e6565] flex justify-center items-center rounded-lg">
        <h2 class="text-lg">{{ number }}</h2>
      </div>
      <h3 class="text-black font-bold">{{ title }}</h3>
      <article class="text-black text-sm font-extralight">{{ description }}</article>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      number: String,
      title: String,
      description: String,
    },
  };
  </script>