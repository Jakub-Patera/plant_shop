<template>
    <section class="flex justify-center  items-center flex-col lg:grid lg:grid-cols-2 lg:px-80 pt-10 text-xl h-[80%] mt-20 mx-auto py-28 ">
      <div class="col-span-1 flex justify-center items-center">
        <div class="mx-auto flex justify-center items-start flex-col md:items-center md:space-y-4">
          <h1 class="text-6xl md:text-3xl font-extrabold leading-[80px] tracking-tighter">The rare plant <br/> scent for your<br> living room </h1>
          <article class="text-left max-w-md">Create incredible plant design for your offices or apartments. Add freshness to your new ideas.</article>
          <button class="bg-[#3e6565] text-white px-6 py-4 mt-8 rounded-xl flex flex-row">Explore <svg-icon class="ml-4 pt-1" type="mdi" :path="path"></svg-icon></button>
        </div>
      </div>
      <div class="col-span-1 flex justify-center items-center order-first md:order-last md:pt-6">
        <img src="../assets/img/home.png" alt="" class="md:w-[350px] w-44  ">
      </div>
    </section>
  </template>
  



<script>
import SvgIcon from '@jamescoyle/vue-icon';
import { mdiArrowBottomRightThick } from '@mdi/js';

export default {
  name: "my-component",
  components: {
    SvgIcon,
  },
  data() {
    return {
      path: mdiArrowBottomRightThick,
    };
  },
};
</script>
