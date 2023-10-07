<template>
    <div id="products" class="flex justify-center items-center my-12 flex-col space-y-11">
      <h1 class="text-center text-4xl font-extrabold">
        Check out our <br />products
      </h1>
      <article class="max-w-[32%] text-center">
        Here are some selected plants from our showroom, all are in excellent
        shape and have a long life span. Buy and enjoy the best quality.
      </article>
      <!-- Products -->
      <div class="grid grid-cols-1 md:grid-cols-3 gap-x-0 gap-y-8">
        <!-- Product Cards -->
        <ProductCard
          image="/assets/img/product1.png"
          title="Cacti Plant"
          price="$5.99"
        />
        <ProductCard
          image="/assets/img/product2.png"
          title="Cacti Plant"
          price="$5.99"
        />
        <ProductCard
          image="/assets/img/product3.png"
          title="Cacti Plant"
          price="$5.99"
        />
        <ProductCard
          image="/assets/img/product4.png"
          title="Cacti Plant"
          price="$5.99"
        />
        <ProductCard
          image="/assets/img/product5.png"
          title="Cacti Plant"
          price="$5.99"
        />
        <ProductCard
          image="/assets/img/product6.png"
          title="Cacti Plant"
          price="$5.99"
        />
      </div>
    </div>
  </template>
  
  <script>
  import ProductCard from "./ProductCard.vue"; // Import the ProductCard component
  
  export default {
    components: {
      ProductCard,
    },
  };
  </script>