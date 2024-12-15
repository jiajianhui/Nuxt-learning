<template>
    <div class="conatiner flex flex-col justify-center items-center min-h-screen bg-[url('/ocean-4.jpg')] bg-cover bg-center bg-fixed">

        <CommonNavbar />


        <slot />
        
        <CommonSocialLinks />

        <CommonFooter />
     </div>
</template>