<template>
    <div class="main font-serif text-center flex flex-col justify-center  text-white min-h-screen">

        <MiniLabel />
        
        <CommonPrimaryTitle />

        <FeaturesBoxContainer>
            <FeaturesBoxHeader />
            <FeaturesBoxDescription />
            <FeaturesBoxJoinButton />
        </FeaturesBoxContainer>

        
    </div>
</template>


<style>
    .main {
        min-height: calc(100vh - 120px);
    }
</style>