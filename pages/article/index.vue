<template>
    <div class="main font-serif text-center flex justify-center  text-white min-h-screen">
        <div class="grid grid-cols-3 gap-8 w-2/3 py-20">
            <ContentList path="/article" v-slot="{ list }">
                <NuxtLink :to="item._path" v-for="item in list" :key="item._path" class="group text-left bg-gradient-to-b from-white/10 backdrop-blur  border rounded-3xl border-white p-6">
                    <div v-if="item.image" class="w-full h-40 rounded-2xl mb-2 overflow-clip">
                        <img :src="item.image" class="group-hover:scale-125 transition-all">
                    </div>
                    
                    <h2 class="text-xl truncate group-hover:underline underline-offset-2 transition-all">{{ item.title }}</h2>
                    <p class="text-sm text-white/70">{{ item.description }}</p>
                </NuxtLink>

                
            </ContentList>
            
        </div>
        
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