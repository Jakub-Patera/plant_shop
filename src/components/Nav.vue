

<template>
  <section class="px-80 lg:px-20 pt-10 text-xl md:flex md:justify-between">
    <div class="flex flex-row items-center justify-center">
      <svg-icon type="mdi" :path="path" class="h-16 w-16"></svg-icon>
     <a href="#">
      <h1 class="uppercase font-extrabold tracking-tighter text-2xl">
       Plantex
     </h1>
    </a> 
      
    </div>

    <div class="col-span-1 lg:flex lg:flex-row lg:justify-end lg:items-center hidden">
      <ul class="flex flex-row space-x-6">
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#products">Products</a></li>
        <li><a href="#">FAQs</a></li>
        <li><a href="#">Contact Us</a></li>
      </ul>
    </div>

    <!-- Mobile Menu -->
    <div class="md:hidden flex justify-center items-center">
      <button
        @click="isOpen = !isOpen"
        type="button"
        class="block text-gray-500 hover:text-white focus:text-white focus:outline-none"
      >
        <svg
          class="h-12 w-12 fill-current"
          viewBox="0 0 24 24"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            v-if="isOpen"
            fill-rule="evenodd"
            clip-rule="evenodd"
            d="M19.293 4.293a1 1 0 0 0-1.414-1.414L12 10.586 5.121 3.707a1 1 0 1 0-1.414 1.414L10.586 12l-6.879 6.879a1 1 0 1 0 1.414 1.414L12 13.414l6.879 6.879a1 1 0 1 0 1.414-1.414L13.414 12l6.879-6.879z"
          />
          <path
            v-else
            fill-rule="evenodd"
            clip-rule="evenodd"
            d="M4 6a1 1 0 0 1 1-1h14a1 1 0 1 1 0 2H5a1 1 0 0 1-1-1zm0 5a1 1 0 0 1 1-1h14a1 1 0 1 1 0 2H5a1 1 0 0 1-1-1zm1 5a1 1 0 1 1 0-2h14a1 1 0 1 1 0 2H5z"
          />
        </svg>
      </button>

      <div
        v-if="isOpen"
        class="fixed top-0 left-0 w-full h-full bg-gray-800 bg-opacity-50 z-50 "
      >
        <div class="p-5 bg-white border rounded shadow-sm absolute w-full justify-center items-center ">
          <button
            @click="isOpen = false"
            type="button"
            class="block text-gray-500 hover:text-white focus:text-white focus:outline-none absolute top-0 right-0 m-4"
          >
            <svg
              class="h-6 w-6 fill-current"
              viewBox="0 0 24 24"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                fill-rule="evenodd"
                clip-rule="evenodd"
                d="M19.293 4.293a1 1 0 0 0-1.414-1.414L12 10.586 5.121 3.707a1 1 0 1 0-1.414 1.414L10.586 12l-6.879 6.879a1 1 0 1 0 1.414 1.414L12 13.414l6.879 6.879a1 1 0 1 0 1.414-1.414L13.414 12l6.879-6.879z"
              />
            </svg>
          </button>
          <ul class="flex flex-col space-y-4 justify-center items-center">
            <li><a href="#">Home</a></li>
            <li><a href="#">About</a></li>
            <li><a href="#products">Products</a></li>
            <li><a href="#">FAQs</a></li>
            <li><a href="#">Contact Us</a></li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import SvgIcon from "@jamescoyle/vue-icon";
import { mdiLeaf, mdiClose, mdiMenu } from "@mdi/js";

export default {
  name: "my-component",
  components: {
    SvgIcon,
  },
  data() {
    return {
      path: mdiLeaf,
      isOpen: false,
    };
  },
};
</script>
