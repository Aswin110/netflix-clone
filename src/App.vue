<script setup>
    import { onMounted, ref } from 'vue';

    import Magnify from 'netflix-clone/node_modules/vue-material-design-icons/Magnify';
    import HomeOutline from 'netflix-clone/node_modules/vue-material-design-icons/HomeOutline';
    import TrendingUp from 'netflix-clone/node_modules/vue-material-design-icons/TrendingUp';
    import Television from 'netflix-clone/node_modules/vue-material-design-icons/Television';
    import MovieOutline from 'netflix-clone/node_modules/vue-material-design-icons/MovieOutline';
    import Plus from 'netflix-clone/node_modules/vue-material-design-icons/Plus';
    import ChevronLeft from 'netflix-clone/node_modules/vue-material-design-icons/ChevronLeft';

    import {useMovieStore} from './stores/movie'
    import { storeToRefs } from 'pinia'
    const useMovie= useMovieStore()
    const {movie,showFullVideo}=storeToRefs(useMovie)
</script>

<template>
  <div class="text-red-400">
    text here
  </div>
</template>

<style scoped>

</style>
