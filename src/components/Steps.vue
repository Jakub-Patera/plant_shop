<template>
    <div class="flex justify-center items-center py-12 pb-20 ">
      <div class="bg-[#3e6565] w-[80%] rounded-2xl text-white py-14 ">
        <h1 class="text-4xl text-center font-semibold">
          Steps to start your<br />plants off right
        </h1>
  
        <div class="flex justify-center items-center  md:space-x-6  space-y-4 py-10 flex-col md:flex-row mx-3">
          <StepsCard
            number="01"
            title="Choose Plant"
            description="We have several varieties plants you can choose from."
          />
          <StepsCard
            number="02"
            title="Place an Order"
            description="Once your order is set, we move to the next step which is the shipping."
          />
          <StepsCard
            number="03"
            title="Get plants delivered"
            description="Our delivery process is easy, you receive the plant direct to your door."
          />
        </div>
      </div>
    </div>
  </template>
  
  <script>
  import StepsCard from "./StepsCard.vue"; // Import the StepCard component
  
  export default {
    components: {
      StepsCard,
    },
  };
  </script>