<script setup lang="ts">
import { Analytics } from '@vercel/analytics/nuxt';

//SEO
useHead({
  // 动态标题
  titleTemplate: '%s - jianhui.fun',
  // 打印
  script: [ { innerHTML: 'console.log(\'Hello world\')' } ]
})
</script>


<template>
  <div>
    <NuxtRouteAnnouncer />
    <!-- <NuxtWelcome /> -->
    <NuxtLayout>
      <Analytics />
      <NuxtPage />
    </NuxtLayout>
  </div>
</template>

