<template>
    <div class="common-navbar flex justify-center items-center pt-6 text-white">
        <ul class="flex justify-center items-center backdrop-blur border rounded-3xl border-white px-8 py-2 ">
            <li class="mr-6">
                <NuxtLink to="/">Home</NuxtLink>
            </li>
            <li class="mr-6">
                <NuxtLink to="/waitlist">Waitlist</NuxtLink>
            </li>
            <li class="">
                <NuxtLink to="/">FAQ</NuxtLink>
            </li>
        </ul>
    </div>
</template>

<style>
    .common-navbar {
        height: 50px;
    }
</style>