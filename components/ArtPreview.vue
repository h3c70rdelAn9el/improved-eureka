<template>
<div class="border border-black shadow-xl">
  <nuxt-link :to="id">
    <article class="rounded border border-black shadow">
      <!-- <div
          class="w-full"
          :style="{background: `url(${artImage})`, backgroundSize: 'cover', height: 200 + 'px', width: 100% + 'px' }"
        /> -->
      <div class="w-full rounded" :style="{backgroundImage: 'url(' + artImage + ')', backgroundSize: 'cover', height: 200 + 'px', width: 100% + 'px' }"></div>
      <!-- <div
      class="w-full"
      :style="{background: `url(${artImage})`, backgroundSize: 'cover', height: 200 + 'px', width: 100% + 'px' }"
    /> -->
      <div>
        <h1 class="text-center text-2xl font-title p-1 text-gray-100 bg-gray-800">{{ title }}</h1>
      </div>
    </article>
  </nuxt-link>
</div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true
    },
    artImage: {
      type: String,
      required: true
    },
    id: {
      type: String,
      required: true
    }
  }
}
</script>

<style scoped>
a {
  text-decoration: none;
  color: black
}
</style>
