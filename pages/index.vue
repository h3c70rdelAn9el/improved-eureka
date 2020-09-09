<template>
  <div class="container mx-auto">
    <div class="block">
      <h1 class="text-4xl mb-1">The Menjou Galerie</h1>
      <p class="mb-1">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Accusantium, dolorum.</p>
      <img  src="../assets/img/gallery.jpg" alt="" style="height: 26rem;">
    </div>

  </div>
</template>

<script>
export default {}
</script>

<style>
/* Sample `apply` at-rules with Tailwind CSS
.container {
@apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.page-enter-active, .page-leave-active {
  transition: opacity 1s;
}
.page-enter, .page-leave-to {
  opacity: 0;
}


</style>
