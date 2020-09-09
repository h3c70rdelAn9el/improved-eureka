<template>
  <nav class="font-heading flex fixed mt-8 justify-between  pb-2 pt-4 px-6 text-center bg-lightbrown bg-opacity-50 w-full z-10 top-0 shadow-2xl">
    <div class="mb-2 sm:mb-0">
      <nuxt-link to="/" class="h-12">
        <!-- <h1 class="font-title text-2xl pl-2 pb-1 text-white">Menjou Galerie</h1> -->
        <img class="h-12" src="../assets/img/logo.png" alt="logo">
      </nuxt-link>
    </div>
    <div class="flex text-white pt-1 mb-0">
      <nuxt-link to="/exhibits" class="rounded p-1 mb-4 text-lg no-underline hover:text-chocolate ml-2">
        Exhibits
      </nuxt-link>
      <nuxt-link to="/comingsoon" class="rounded p-1 mb-4 h-13text-lg no-underline hover:text-chocolate ml-2">
        Coming Soon
      </nuxt-link>
      <nuxt-link to="/contact" class="rounded p-1 mb-4 text-lg no-underline hover:text-chocolate ml-2">
        Contact
      </nuxt-link>
    </div>
  </nav>
</template>
