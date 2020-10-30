<template>
<div>
  <div class="-mt-4">
    <h1 class="text-3xl text-center text-gray-100 font-title">Surreal Gallerie</h1>
  </div>
  <hr class="border border-black">
  <div class="w-full mt-2 flex-row sm:flex  pb-4">
    <div v-for="work in works" :id="work.id" :key="work.id" class="w-full p-2 rounded shadow-lg">
      <ArtPreview class="rounded" :id="work.id" :key="work.id" :title="work.title" :artImage="work.artImage" />
    </div>
  </div>
  <div class="mt-4">
    <nuxt-link class="rounded p-2 bg-gray-800 text-gray-100 hover:bg-gray-600 hover:text-black" to="/exhibits">
      Back to Exhibits
    </nuxt-link>
  </div>

</div>
</template>

<script>
import ArtPreview from '@/components/ArtPreview'

export default {
  components: {
    ArtPreview
  },
  asyncData(context) {
    return context.app.$storyapi.get('cdn/stories/', {
        version: 'draft',
        starts_with: 'collection/'
      })
      .then(res => {
        return {
          works: res.data.stories.map(cp => {
            return {
              id: cp.slug,
              title: cp.content.title,
              description: cp.content.description,
              artImage: cp.content.artImage
            }
          })
        };
      })
  }
}
</script>
