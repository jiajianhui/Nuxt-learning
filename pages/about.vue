<template>
    <div class="main font-serif text-center flex flex-col justify-center  text-white min-h-screen">

        <MiniLabel />
        
        <CommonPrimaryTitle />

        <FeaturesBoxContainer>
            <FeaturesBoxHeader />
            <FeaturesBoxDescription />
            <UButton to="/" size="lg" color="black" variant="solid">返回首页</UButton>
        </FeaturesBoxContainer>

        
    </div>
</template>

<script>
  definePageMeta({
    layout: 'about'
  })
</script>


<style>
    .main {
        min-height: calc(100vh - 150px);
    }
</style>