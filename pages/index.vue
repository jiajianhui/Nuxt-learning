<template>
  <div class="conatiner flex justify-center items-center min-h-screen bg-[url('/ocean-1.jpg')] bg-cover bg-center">
    <div class="font-serif text-center text-white ">

        <div class="flex justify-center items-center -translate-y-12 ">
            <div class="flex justify-center items-center px-5 py-2 backdrop-blur-sm border border-white rounded-full">
                <UIcon name="i-mdi-airplane-takeoff" class="mr-2 w-6 h-6" />
                <span class="text-xl font-light">hello nuxt</span>  
            </div>
        </div>
        
        <h1 class="text-9xl translate-y-10">Coming Soon</h1>

        <div class="flex justify-center items-center ">
            <div class="flex flex-col justify-center items-center px-10 py-14 bg-gradient-to-b from-white/10 backdrop-blur  border rounded-3xl border-white">
                <h2 class="text-4xl font-bold mb-3">开启我的Nuxt学习之旅 🎉</h2>
                <p class="text-white/70 text-l mb-8">
                    我正在学习Nuxt，我将通过这个项目来记录我的学习过程。
                </p>
                <UButton size="lg" color="black" variant="solid">立即加入</UButton>
            </div>
        </div>

         <div class="flex justify-center items-center mt-10 ">
            <div class="flex [&>*:not(:last-child)]:mr-6">
                <a href="http://" title="github" target="_blank" class="text-white/70 hover:text-white transition-all duration-300">
                    <UIcon name="i-mdi-github" class="w-8 h-8" />
                </a>
                <a href="http://" title="pinterest" target="_blank" class="text-white/70 hover:text-white transition-all duration-300">
                    <UIcon name="i-mdi-pinterest" class="w-8 h-8" />
                </a>
                <a href="http://" title="spotify" target="_blank" class="text-white/70 hover:text-white transition-all duration-300">
                    <UIcon name="i-mdi-spotify" class="w-8 h-8" />
                </a>
            </div>
        </div>

        
    </div>
  </div>
</template>
