<template>
<div class="relative flex flex-wrap w-full">
  <div v-for="(item, index) in items" :key="index" class="absolute w-full">
    <transition name="fade">

      <div v-if="currentSlide === index" class="w-full" :class="item" style="height:400px">
        <img :src="item.src" alt="" class="h-full w-full">
      </div>
    </transition>
  </div>
  <!-- Nav buttons -->
  <div class=" w-full" style="height: 390px">
    <div class="absolute bottom-0 flex w-full justify-center">

      <div v-for="(item, index) in items" :key="index" @click="makeActive(index)" :class="currentSlide === index ? 'bg-gray-700' : 'bg-gray-200'" class="w-2 mx-1 h-2 rounded-full cursor-pointer">
      </div>

    </div>
  </div>
</div>
</template>

<script>
export default {
  data() {
    return {
      currentSlide: 0,
      items: [{
          src: require('../assets/img/gallery.jpg')
        },
        {
          src: require('../assets/img/gallery-two.jpg')
        },
        {
          src: require('../assets/img/gallery-three.jpg')
        }
      ],
      interval: '',
      isDetailsShowing: true
    }
  },
  mounted() {
    this.interval = setInterval(() => {
      this.currentSlide = this.currentSlide === 2 ? 0 : this.currentSlide + 1
    }, 4000)
  },
  beforeUnmount() {
    clearInterval(this.interval)
  },
  methods: {
    makeActive(index) {
      this.currentSlide = index
    }
  },
}
</script>

<style>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 1s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>
