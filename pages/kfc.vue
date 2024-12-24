<template>
    <div class="main font-serif text-center flex flex-col justify-center  text-white min-h-screen">

        
        <CommonPrimaryTitle />

        <FeaturesBoxContainer>
            <div class="markdown-body">
                <ContentRendererMarkdown :value="randomArticle"/>
            </div>
            
        </FeaturesBoxContainer>

        
    </div>
</template>


<script setup lang="ts">

// // 随机查询内容
// const aaa = await queryContent('kfc').find()
// const randomArticle = ref(null);
// randomArticle.value = aaa[0]


const randomArticle = ref(null)
// 查询文件数
const count = await queryContent('kfc').count()

// 生成随机数
const randomIndex = Math.floor(Math.random() * count)

// 查询所有数据
const articles = await queryContent('kfc').find()
randomArticle.value = articles[randomIndex]




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