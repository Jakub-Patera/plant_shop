<template>
  <section class="px-80 lg:px-20 pt-10 text-xl md:flex md:justify-between">
    <div class="flex flex-row items-center justify-center">
      <svg-icon type="mdi" :path="path" class="h-16 w-16"></svg-icon>
      <h1 class="uppercase font-extrabold tracking-tighter text-2xl">
        Plantex
      </h1>
    </div>

  
    <div
  
      class="col-span-1 lg:flex lg:flex-row lg:justify-end lg:items-center hidden"
    >
      <ul class="flex flex-row space-x-6">
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#products">Products</a></li>
        <li><a href="#">FAQs</a></li>
        <li><a href="#">Contact Us</a></li>
      </ul>
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
      
    };
  },
};
</script>
