<template>
    <div class="flex flex-col md:flex-row md:justify-evenly items-center py-8 md:py-32 px-4 md:px-32 lg:px-64">
      <div class="w-full md:w-1/4 flex flex-col items-center">
        <h1 class="font-bold mb-3">
          <svg-icon type="mdi" :path="path" class="h-4 w-4 mr-2"></svg-icon>
          PLANTEX
        </h1>
        <div class="flex flex-col items-center">
          <h1 class="font-semibold mb-3 text-center">
            Subscribe to our newsletter to stay updated
          </h1>
          <div class="w-full md:w-[80%]">
            <button
              type="submit"
              class="bg-[#3e6565] text-white py-3 px-2 rounded-xl w-full"
            >
              <input
                placeholder="Email"
                type="email"
                id="email"
                v-model="email"
                required
                class="border-b-blue-gray-700 border-b-2 text-gray-700 text-sm focus-visible:outline-none bg-transparent focus-visible:text-white w-full"
              />
              Subscribe
            </button>
          </div>
        </div>
      </div>
  
      <!-- Address -->
      <div class="w-full md:w-1/4 mt-6 md:mt-0 flex flex-col items-center">
        <h1 class="font-bold mb-3">Our Address</h1>
        <div class="flex flex-col items-center text-center">
          <p class="text-gray-800 mb-2 font-light">123 Main St.</p>
          <p class="text-gray-800 mb-2 font-light">Anytown, USA 12345</p>
          <p class="text-gray-800 mb-2 font-light">Phone: 555-555-5555</p>
        </div>
      </div>
  
      <!-- Contact with social icons -->
      <div class="w-full md:w-1/4 mt-6 md:mt-0 flex flex-col items-center">
        <p class="text-gray-800 mb-4">Follow us on social media:</p>
        <div class="flex space-x-3">
          <a href="" class="">
            <svg-icon type="mdi" :path="facebookPath"></svg-icon>
          </a>
          <a href="">
            <svg-icon type="mdi" :path="instagramPath"></svg-icon>
          </a>
          <a href="">
            <svg-icon type="mdi" :path="youtubePath"></svg-icon>
          </a>
        </div>
      </div>
  
      <!-- Images of credit cards -->
      <div class="w-full md:w-1/4 mt-6 md:mt-0 flex flex-col items-center">
        <h1 class="text-center">We accept all credit cards</h1>
        <div class="flex flex-row items-center">
          <img src="/assets/img/visa.png" alt="Visa" class="w-16 h-16 mx-2" />
          <img
            src="/assets/img/mastercard.png"
            alt="Mastercard"
            class="w-16 h-12 mx-2"
          />
          <img
            src="/assets/img/amex.png"
            alt="American Express"
            class="w-16 h-16 mx-2"
          />
        </div>
      </div>
    </div>
  </template>
  

<script>
import SvgIcon from "@jamescoyle/vue-icon";
import { mdiFacebook, mdiInstagram, mdiYoutube, mdiLeaf } from "@mdi/js";
export default {
  components: {
    SvgIcon,
  },
  data() {
    return {
      email: "",
      facebookPath: mdiFacebook,
      instagramPath: mdiInstagram,
      youtubePath: mdiYoutube,
      path: mdiLeaf,
    };
  },
  methods: {
    subscribe() {
      // Handle email subscription here
      console.log("Email subscribed:", this.email);
    },
  },
};
</script>
