<template>
    <div class="main font-serif text-center flex justify-center  text-white min-h-screen">

        <FeaturesBoxContainer class="w-2/3">
            <ContentDoc class="text-white/70 text-l mb-8" />
            <UButton to="/article" size="lg" color="black" variant="solid">回到文章列表</UButton>
        </FeaturesBoxContainer>
        
        

        
    </div>
</template>

<script setup lang="ts">
definePageMeta({
  layout: 'article'
})
</script>


<style>
    .main {
        min-height: calc(100vh - 150px);
    }
</style>