<template>
<div>
  <h1 class="text-black text-3xl text-center font-title">Coming Soon</h1>
  <div class="p-2">
    <div class="p-2 border bg-gray-300 opacity-75 border-black rounded my-2" v-for="post in posts" :key="post.id">
      <h1 class="text-3xl font-title text-gray-900">{{ post.title }}</h1>
      <hr class="border border-black">
      <p class="p-2 text-lg text-black">{{ post.intro }}</p>
      <div class="w-full border border-black shadow-sm rounded" :style="{backgroundImage: 'url(' + post.image + ')', backgroundSize: 'cover', height: 200 + 'px', width: 100% + 'px' }"></div>
      <div>
        <p class="p-2 text-sm text-black">{{ post.text }}</p>
      </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  asyncData(context) {
    return context.app.$storyapi.get('cdn/stories', {
        version: 'draft',
        starts_with: 'coming-soon'
      })
      .then(res => {
        return {
          posts: res.data.stories.map(sp => {
            return {
              id: sp.slug,
              title: sp.content.title,
              intro: sp.content.intro,
              image: sp.content.image,
              text: sp.content.Text
            }
          })
        }
      })
  }
}
</script>
