<template>
  <nav class="font-heading flex fixed mt-8 justify-between  py-4 px-6 text-center bg-lightbrown  w-full z-10 top-0 shadow-2xl">
    <div class="mb-2 sm:mb-0">
      <nuxt-link to="/" class="w-50 h-50">
        <h1 class="text-2xl pl-2 pb-1 text-white">Galerie</h1>
      </nuxt-link>
    </div>
    <div class="flex text-white">
      <nuxt-link to="/about" class="rounded p-1 text-lg no-underline text-white hover:bg-chocolate ml-2">
        About
      </nuxt-link>
      <nuxt-link to="/exhibits" class="rounded p-1 text-lg no-underline hover:bg-chocolate ml-2">
        Exhibits
      </nuxt-link>
      <nuxt-link to="/comingsoon" class="rounded p-1 text-lg no-underline hover:bg-chocolate ml-2">
        Coming Soon
      </nuxt-link>
      <nuxt-link to="/contact" class="rounded p-1 text-lg no-underline hover:bg-chocolate ml-2">
        Contact
      </nuxt-link>
    </div>
  </nav>
</template>
