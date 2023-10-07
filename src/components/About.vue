<template>
    <section class=" pt-10 text-xl h-[80%] mt-20  py-28 ">
        <div class=" flex justify-center items-center">

            <div class="grid grid-cols-2 grid-flow-row">
              <div class="col-span-1">
                <img src="../assets/img/about.png" alt="" class="h-96" />
              </div>
              <div class="col-span-1">
                <h1 class="text-3xl font-extrabold tracking-tighter">
                  Who we really are &<br />
                  why choose us <br />
                </h1>
                <article class="max-w-[470px] text-md mt-9">
                  We have over 4000+ unbiased reviews and our customers trust our plant
                  process and delivery service every time
                </article>
                <div class="mt-8 space-y-4">
                  <p class="text-sm flex items-center">
                    <svg-icon type="mdi" :path="path"></svg-icon>We always deliver on time.
                  </p>
                  <p class="text-sm flex items-center">
                    <svg-icon type="mdi" :path="path"></svg-icon>We always deliver on time.
                  </p>
                  <p class="text-sm flex items-center">
                    <svg-icon type="mdi" :path="path"></svg-icon>We always deliver on time.
                  </p>
                  <p class="text-sm flex items-center">
                    <svg-icon type="mdi" :path="path"></svg-icon>We always deliver on time.
                  </p>
                </div>
                <a href="http://" rel="noopener noreferrer" class="flex justify-start pt-10">Shop Now <svg-icon class="ml-4 pt-1" type="mdi" :path="path"></svg-icon></a>
              </div>
            </div>
        </div>

    </section>
  </template>
  


<script>
import SvgIcon from '@jamescoyle/vue-icon';
import { mdiCheckboxMarked } from '@mdi/js';
import { mdiArrowBottomRight } from '@mdi/js';

export default {


	components: {
		SvgIcon
	},

	data() {
		return {
	  		path: mdiCheckboxMarked,
              path: mdiArrowBottomRight,
		}
	}
}
</script>


