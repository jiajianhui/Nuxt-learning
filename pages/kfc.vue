<template>
    <div class="main font-serif text-center flex flex-col justify-center  text-white min-h-screen">

        
        <CommonPrimaryTitle />

        <FeaturesBoxContainer>
            <div class="markdown-body" v-if="randomArticle">
                <ContentRendererMarkdown :value="randomArticle"/>
            </div>
            
        </FeaturesBoxContainer>

        
    </div>
</template>


<script setup lang="ts">


const randomArticle = ref(null)

// 随机获取文章函数
const getRandomArticle = async () => {
    const count = await queryContent('kfc').count()

    const randomIndex = Math.floor(Math.random() * count)

    const articles = await queryContent('kfc').find()

    randomArticle.value = articles[randomIndex]
}

// 组件挂载后执行获取数据；不会在服务器端进行渲染，否则会渲染两次
onMounted(getRandomArticle)


definePageMeta({
  layout: 'article'
})
</script>




<style>
    .main {
        min-height: calc(100vh - 150px);
    }
    .markdown-body {
        background: none;
        text-align: start;
        color: white;
    }
    
</style>