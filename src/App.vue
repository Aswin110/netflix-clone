<script setup>
    import { onMounted, ref } from 'vue';

    import Magnify from 'vue-material-design-icons/Magnify.vue';
    import HomeOutline from 'vue-material-design-icons/HomeOutline.vue'
    import TrendingUp from 'vue-material-design-icons/TrendingUp.vue'
    import Television from 'vue-material-design-icons/Television.vue'
    import MovieOutline from 'vue-material-design-icons/MovieOutline.vue'
    import Plus from 'vue-material-design-icons/Plus.vue'
    import ChevronLeft from 'vue-material-design-icons/ChevronLeft.vue'

    import {useMovieStore} from './stores/movie'
    import { storeToRefs } from 'pinia'
    const useMovie= useMovieStore()
    const {movie,showFullVideo}=storeToRefs(useMovie)
</script>

<template>
  <div class="fixed w-full h-screen bg-black"> 
    <div v-if="!showFullVideo" id="sideNav" class="flex z-40 items-center w-[120p] h-screen bg-black relative">
      N
      <div>
        <div class="py-2 mx-10 my-6">
          <Magnify fillColor="#ffffff" :size="40" class="cursor-pointer" />
        </div>
        <div class="py-2 mx-10 my-6 border-b-4 border-b-red-500">
          <HomeOutline fillColor="#ffffff" :size="40" class="cursor-pointer" />
        </div>
        <div class="py-2 mx-10 my-6">
          <TrendingUp fillColor="#ffffff" :size="40" class="cursor-pointer" />
        </div>
        <div class="py-2 mx-10 my-6">
          <Television fillColor="#ffffff" :size="40" class="cursor-pointer" />
        </div>
        <div class="py-2 mx-10 my-6">
          <MovieOutline fillColor="#ffffff" :size="40" class="cursor-pointer" />
        </div>
        <div class="py-2 mx-10 my-6">
          <Plus fillColor="#ffffff" :size="40" class="cursor-pointer" />
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>

</style>
