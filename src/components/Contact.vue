<template>
    <div class="h-auto flex flex-col justify-center my-32  mx-6 items-center space-y-6 md:flex-row md:items-center space-x-6 md:space-x-16">
        <article class="space-y-4 max-w-prose text-center md:text-left">
      <h1 class="text-3xl font-semibold">
        Reach out to us today via any of the given information
      </h1>

      <div class="pb-6">
        <span class="font-medium">Call us for instant support</span> <br />
        <div class="flex md:block justify-center items-center flex-row">
          <a href="tel:+11111111111111" class="flex flex-row space-x-2 items-center">
            <svg-icon type="mdi" :path="phonePath"></svg-icon>
            <p>+ 111 111 111 111 11</p>
          </a>
        </div>
      </div>
      <div class="font-extralight">
        <span class="font-medium">Write us by mail</span> <br />
        <div class="flex md:block justify-center items-center flex-row">
          <a href="mailto:email@email.com" class="flex flex-row space-x-2 items-center">
            <svg-icon type="mdi" :path="emailPath"></svg-icon>
            <p>email@email.com</p>
          </a>
        </div>
      </div>
    </article>
      <!-- contact form -->
      <div class="h-auto">
        <form
          @submit.prevent="submitForm"
          class="space-y-3 flex justify-center items-start flex-col max-w-prose"
        >
          <input
            placeholder="Name"
            type="text"
            id="name"
            v-model="name"
            required
            class="border-b-blue-gray-700 border-b-2 text-gray-700 focus-visible:outline-none"
          />
  
          <input
            placeholder="Email"
            type="email"
            id="email"
            v-model="email"
            required
            class="border-b-blue-gray-700 border-b-2 text-gray-700 focus-visible:outline-none"
          />
  
          <textarea
            placeholder="Message"
            id="message"
            v-model="message"
            required
            class="border-b-blue-gray-700 border-b-2 text-gray-700 focus-visible:outline-none mb-6"
          ></textarea>
          <button
            type="submit"
            class="bg-[#3e6565] text-white py-3 px-6 rounded-xl "
          >
            Send Message
          </button>
        </form>
      </div>
    </div>
  </template>
  

<script>
import SvgIcon from "@jamescoyle/vue-icon";
import { mdiPhone } from "@mdi/js";
import { mdiEmailOutline } from "@mdi/js";

export default {
  components: {
    SvgIcon,
  },

  data() {
    return {
      name: "",
      email: "",
      message: "",
      emailPath: mdiEmailOutline,
      phonePath: mdiPhone,
    };
  },
  methods: {
    submitForm() {
      // Handle form submission here
      console.log("Form submitted!");
      console.log("mame: " + this.name);
      console.log("email: " + this.email);
      console.log("message: " + this.message);
    },
  },
};
</script>
