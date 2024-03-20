<template>
    <div>
            <!-- Main navbar -->
            <div>
            <header class="shadow-sm bg-white">
            <nav class="p-4 mx-auto flex justify-between">
                <NuxtLink to="/" class="text-2xl font-semibold hover:font-bold"> Nuxt Demo </NuxtLink>
                <ul class="flex md:gap-6 sm:gap-2 2xs:gap-1">
                <li><NuxtLink to="/">Home</NuxtLink></li>
                <li><NuxtLink to="/about">About</NuxtLink></li>
                <li><NuxtLink>Contacts</NuxtLink></li>
                <li><NuxtLink>Logout</NuxtLink></li>
                </ul>
            </nav>
            </header>
            </div>

            <div class="container mx-auto">
                <slot/>
            </div>
    </div>
</template>

<script setup>

</script>

<style scoped>

li:hover{
    color: rgb(0, 145, 48);
    cursor: pointer;
}

#sideNav{
    max-width: 300px;
    min-height: 300px;
}

</style>