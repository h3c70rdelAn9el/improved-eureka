<template>
<div class="flex justify-between bg-chocolate h-full text-white">
  <div class="p-4">
    <p class="text-base">The Menjour Galerie &copy; 2020</p>
    <hr>
    <section class="text-xs">
      <p>All images from the awesome <a href="https://unsplash.com/">unsplash.com</a></p>
      <p>Logo made from <a href="https://logomakr.com/">LogoMakr.com</a></p>
      <p>Favicon provided by <a href="https://favicon.io/">favicon.io</a></p>
    </section>
  </div>
  <div class="flex flex-col p-4 mr-5">
    <div class="text-lg text-right">
      <a href="" class="hover:text-lightbrown">

        <fa :icon="['fab', 'instagram']" class="mr-2" />
      </a>
      <a href="" class="hover:text-lightbrown">
        <fa :icon="['fab', 'twitter']" class="mr-2" />
      </a>
      <a href="" class="hover:text-lightbrown">
        <fa :icon="['fab', 'etsy']" class="mr-2" />
      </a>
    </div>
    <hr>
    <div>
      <p class="text-xs text-right">Sample site made by <a href="https://github.com/h3c70rdelAn9el">Hector</a><br> with the power of <a href="https://nuxtjs.org/" target="_blank">NuxtJS!</a></p>
    </div>
  </div>

</div>
</template>
