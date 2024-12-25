<template>
    <div class=" mb-10 w-full font-serif text-center flex flex-col justify-center items-center text-white min-h-screen">

        <CommonPrimaryTitle />

        <FeaturesBoxContainer class="w-full px-10 md:w-3/4 lg:w-1/2 xl:w-2/3 ">
            <!-- loading -->
             <div v-if="isLoading" class="text-center">
                <div class="spinner"></div>
                <p class="mt-4 text-center w-full">静心等待，即将呈现...</p>
            </div>

            <!-- artilce -->
            <div class="markdown-body" v-else-if="randomArticle">
                <ContentRenderer :value="randomArticle">
                    <img :src="randomArticle.image " :alt="randomArticle.title" class="w-full h-[240px] rounded-xl object-cover" >
                    <ContentRendererMarkdown :value="randomArticle"/>
                </ContentRenderer>
                
            </div>
            
            <!-- button -->
            <button @click="refreshRandomArticle" class="px-6 py-2 mt-6 border rounded-md">随机更新文章</button>
        </FeaturesBoxContainer>

        
    </div>
</template>


<script setup lang="ts">

// 随机获取文章函数
const randomArticle = ref(null)

const getRandomArticle = async () => {
    const count = await queryContent('kfc').count()

    const randomIndex = Math.floor(Math.random() * count)

    const articles = await queryContent('kfc').find()

    isLoading.value = false

    randomArticle.value = articles[randomIndex]
}

// 组件挂载后执行获取数据；不会在服务器端进行渲染，否则会渲染两次
onMounted(getRandomArticle)



// 更新文章
const isLoading = ref(true)

const refreshRandomArticle = () => {
    isLoading.value = true
    
    setTimeout(() => {
        getRandomArticle()
    }, 1000);
}


definePageMeta({
  layout: 'article'
})
</script>




<style>
    .markdown-body {
        background: none;
        text-align: start;
        color: white;
    }

    .spinner {
        border: 4px solid rgba(255, 255, 255, 0.3);
        border-radius: 50%;
        border-top: 4px solid #ffffff;
        width: 40px;
        height: 40px;
        animation: spin 1.2s ease-in-out infinite;
        margin: 0 auto;
    }

    @keyframes spin {
        0% { transform: rotate(0deg); }
        100% { transform: rotate(360deg); }
    }
    
</style>