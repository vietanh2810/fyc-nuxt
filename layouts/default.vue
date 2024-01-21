<script setup>
    const menuItems = [
        { path: '/', name: 'Home' },
        { path: '/category/head', name: 'Head' },
        { path: '/category/body', name: 'Body' },
        { path: '/category/other', name: 'Other' },
    ]
</script>

<template>
    <div class="h-full flex">
        <div class="fixed top-0 bottom-0 left-0 w-64 py-5 bg-primary">
            <h1 class="mt-5 font-bold text-center text-3xl">ESGI Merch</h1>

            <ul class="menu mt-4 w-full">
                <li v-for="(menuItem, key) in menuItems" :key="key">
                    <nuxt-link :to="menuItem.path"
                    :class="menuItem.path === $route.path ? 'active block py-2 px-4 text-sm hover:bg-gray-200' : 'block py-2 px-4 text-sm hover:bg-gray-200'">
                        {{ menuItem.name }}
                    </nuxt-link>
                </li>
                <!-- <li><a class="active">Item 2</a></li>
                <li><a>Item 3</a></li> -->
            </ul>
        </div>

        <div class="w-full pl-64 mx-4 mt-4">
            <div>
                <slot></slot>
            </div>
        </div>
    </div>
</template>