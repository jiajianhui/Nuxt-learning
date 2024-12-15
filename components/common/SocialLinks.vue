<template>
    <div class="common-social-links flex justify-center items-center ">
        <div class="flex justify-center items-center [&>*:not(:last-child)]:mr-6 pt-[20px]">
            <a href="http://" title="github" target="_blank" class="w-8 h-8 text-white/70 hover:text-white transition-all duration-300">
                <UIcon name="i-mdi-github" class="w-8 h-8" />
            </a>
            <a href="http://" title="pinterest" target="_blank" class="w-8 h-8 text-white/70 hover:text-white transition-all duration-300">
                <UIcon name="i-mdi-pinterest" class="w-8 h-8" />
            </a>
            <a href="http://" title="spotify" target="_blank" class="w-8 h-8 text-white/70 hover:text-white transition-all duration-300">
                <UIcon name="i-mdi-spotify" class="w-8 h-8" />
            </a>
        </div>
    </div>
</template>


<style>
    .common-social-links {
        height: 40px;
    }
</style>