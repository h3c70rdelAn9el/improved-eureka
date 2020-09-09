<template>
  <div class="flex flex-col min-h-screen font-body w-full bg-repeat-y  " :style="{'background-image': `url(${require('@/assets/img/background.jpg')})`}">
    <Header/>
    <!-- <Nuxt class="pt-32 w-10/12 mx-auto" /> -->
    <transition
      name="fade"
      mode="out-in"
    >
    
      <Nuxt class="pt-40 w-10/12 mx-auto flex-grow"/>
    </transition>
    <Footer class="mt-8"/>
  </div>
</template>

<style>
  /* .page-enter-active, .page-leave-active {
  transition: opacity 1s;
}
.page-enter, .page-leave-to {
  opacity: 0;
} */
.fade-enter-active,
.fade-leave-active {
  transition-duration: .5s;
  transition-property: opacity;
  transition-timing-function: ease;
}

.fade-enter,
.fade-leave-active {
  opacity: 0
}
</style>
