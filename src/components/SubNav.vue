<script setup lang="ts">
import { useRoute } from 'vue-router/auto'

const inactiveStyle = 'opacity-20 hover:opacity-50'
const activeStyle = 'opacity-100 underline'

const route = useRoute()
</script>

<template>
  <div class="prose m-auto mb-8 select-none animate-none! op100!">
    <div mb-0 flex="~ col gap-1 sm:row sm:gap-3 wrap" text-3xl>
      <RouterLink to="/posts" class="!border-none" :class="route.path === '/posts' ? activeStyle : inactiveStyle">
        博客
      </RouterLink>
      <RouterLink to="/notes" class="!border-none" :class="route.path === '/notes' ? activeStyle : inactiveStyle">
        笔记
      </RouterLink>
      <RouterLink to="/life" class="!border-none" :class="route.path === '/life' ? activeStyle : inactiveStyle">
        生活
      </RouterLink>
    </div>
  </div>
</template>
