<template>
<div class="relative flex flex-wrap w-full">
  <!--
  <div v-for="(color, index) in slides" :key="color" class="absolute w-full">
    <transition name="fade">

      <div v-if="currentSlide === index" class=" w-full" :class="color" style="height:350px"></div>
    </transition>
  </div>
  -->
  <!--
  <div v-for="(item, index) in items" :key="index">
    <img :src="item.src" alt="" style="width:100%">
  </div>
  -->
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
<!--
<div class="my-3 flex w-full">
  <div>
    <transition name="fade">
      <h1 v-if="isDetailsShowing" class="text-center">
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Autem, quia.
      </h1>

    </transition>
    <div>
      <button @click="isDetailsShowing = !isDetailsShowing" class="px-2 rounded border">Toggle information</button>
    </div>
  </div>
</div>
-->
</template>

<script>
import image1 from '~/assets/img/abstract1.jpg'
import image2 from '~/assets/img/surreal1.jpg'
import image3 from '~/assets/img/abstract2.jpg'

export default {
  data() {
    return {
      currentSlide: 0,
      items: [{
          src: require('../assets/img/abstract2.jpg')
        },
        {
          src: require('../assets/img/surreal2.jpg')
        },
        {
          src: require('../assets/img/abstract3.jpg')
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
