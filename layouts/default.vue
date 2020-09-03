<template>
  <div class="flex flex-col min-h-screen font-body w-full bg-repeat-y  " :style="{'background-image': `url(${require('@/assets/img/background.jpg')})`}">
    <Header/>
    <!-- <Nuxt class="pt-32 w-10/12 mx-auto" /> -->
    <Nuxt class="pt-40 w-10/12 mx-auto flex-grow"/>
    <Footer class="mt-8"/>
  </div>
</template>
