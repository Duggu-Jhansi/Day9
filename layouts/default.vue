<template>
    <main>

        
        <header class="shadow-sm bg-white">
            <nav class="container mx-auto p-4 flex justify-between">
                <NuxtLink to="/" class="font-bold">NUXT </NuxtLink>
                <ul class="flex gap-4">
                    <li><NuxtLink to="/">Home</NuxtLink>  </li>
                    <li> <NuxtLink to="/about">About</NuxtLink></li>
                    
                    <li><NuxtLink to="episodes" class="btn">Episodes</NuxtLink></li>
                 
                </ul>
            </nav>
            </header>
        
    
    <div class="container mx-auto p-4">
        <slot/>
    </div>
    </main>

    </template>
    <style scoped>
    .router-link-exact-active{
        color:#0077b6;
    }
    .btn{
        @apply bg-[#0077b6] text-white px-3 py-2 rounded-md text-sm text-white;
    }
</style>