<template>
<div>
  <div class="mb-4 -mt-4 mx-auto px-4 md:px-8">
    <h1 class="text-4xl pb-2 font-title text-center">Exhibits</h1>
    <div class="flex flex-wrap -mx-1 lg:-mx-4">
      <!--1st Column -->
      <div class="my-1 px-1 w-full md:w-1/2 lg:my-4 lg:px-4 lg:w-1/3">
        <!-- Article -->
        <section class="overflow-hidden rounded-lg shadow-lg">
          <nuxt-link to="/exhibits/surreal">
            <img alt="Surreal" class="block h-64 w-full rounded-lg shadow-xl" src="~/assets/img/surreal1.jpg">
          </nuxt-link>
          <header class="bg-lightbrown opacity-75 p-2 md:p-4">
            <h1 class="text-2xl text-center">
              <nuxt-link class="no-underline font-heading tracking-wide hover:text-lightbrown hover:bg-chocolate text-black text-center" to="/exhibits/surreal">
                Surreal Galerie
              </nuxt-link>
            </h1>
            <p class="text-center font-body">
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Atque, accusamus.
            </p>
          </header>
        </section>
      </div>
      <!-- End 1st Column -->

      <!-- 2nd Column -->
      <div class="my-1 px-1 w-full md:w-1/2 lg:my-4 lg:px-4 lg:w-1/3">
        <!-- Article -->
        <section class="overflow-hidden rounded-lg shadow-lg">
          <nuxt-link to="/exhibits/abstract">
            <img alt="abstract" class="block h-64 w-full rounded-lg shadow-xl" src="~/assets/img/abstract1.jpg">
          </nuxt-link>
          <header class="bg-lightbrown opacity-75 p-2 md:p-4">
            <h1 class="text-2xl text-center">
              <nuxt-link class="no-underline font-heading tracking-wide hover:text-lightbrown hover:bg-chocolate text-black text-center" to="/exhibits/abstract">
                Abstract Galerie
              </nuxt-link>
              <!--
              <nuxt-link to="/exhibits/abstract">
                Abstract
              </nuxt-link>
              -->
            </h1>
            <p class="text-center font-body">
              Lorem ipsum dolor sit, amet consectetur adipisicing elit. Nam, illo quasi.
            </p>
          </header>
        </section>
      </div>
      <!-- END 2nd Column -->
    </div>
  </div>
</div>
</div>
</template>

<script>
export default {
  transition: {
    name: 'test',
    mode: 'out-in',
    duration: "500"
  }
}
</script>
