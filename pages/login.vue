<template>
    <div class="grid grid-cols-2 h-screen">
        <!-- navbar -->
        <div class="fixed flex items-center bg-gray-100 dark:bg-gray-950 dark:bg-opacity-50 backdrop-blur bg-opacity-50 rounded-lg top-5 left-1/2 -translate-x-1/2 p-2">
            <div class="flex items-center gap-2">
                <NuxtImg class="object-contain w-7" src="/bpd.png" />
                <div class="flex items-center gap-5 text-black dark:text-white">
                    <h2 class="text-md">S-MEBB ADMIN DASHBOARD</h2>
                    <div @click="$colorMode.preference = 'dark'" v-if="$colorMode.preference == 'light'">
                        <tippy content="Switch Dark Mode" class="flex items-center cursor-pointer">
                            <Icon name="material-symbols:wb-sunny-outline" class="text-2xl"/>
                        </tippy>
                    </div>
                    <div @click="$colorMode.preference = 'light'" v-if="$colorMode.preference == 'dark'">
                        <tippy content="Switch Light Mode" class="flex items-center cursor-pointer">
                            <Icon name="material-symbols:nightlight-outline" class="text-2xl -rotate-45"/>
                        </tippy>
                    </div>
                </div>
            </div>
        </div>
        <!-- form -->
        <div class="w-full flex flex-col justify-center p-32 bg-white dark:bg-gray-900">
            <h1 class="text-[#019966] font-bold text-3xl text-center dark:text-green-500">Welcome Back</h1>
            <h2 class="text-gray-600 text-sm mt-1 text-center dark:text-gray-400">Enter your username and password to sign in</h2>
            <form action="" class="mt-8 flex flex-col gap-3">
                <div>
                    <label for="first_name" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">Username</label>
                    <input type="text" id="first_name" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-green-500 focus:border-green-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-green-500 dark:focus:border-green-500" placeholder="Your Username" required />
                </div>
                <div>
                    <label for="first_name" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">Password</label>
                    <input type="password" id="first_name" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-green-500 focus:border-green-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-green-500 dark:focus:border-green-500" placeholder="&#9679;&#9679;&#9679;&#9679;&#9679;" required />
                </div>
                <label class="inline-flex items-center cursor-pointer my-3 w-fit">
                    <input type="checkbox" value="" class="sr-only peer">
                    <div class="relative w-11 h-6 bg-gray-200 peer-focus:outline-none peer-focus:ring-4 peer-focus:ring-green-300 dark:peer-focus:ring-green-800 rounded-full peer dark:bg-gray-700 peer-checked:after:translate-x-full rtl:peer-checked:after:-translate-x-full peer-checked:after:border-white after:content-[''] after:absolute after:top-[2px] after:start-[2px] after:bg-white after:border-gray-300 after:border after:rounded-full after:h-5 after:w-5 after:transition-all dark:border-gray-600 peer-checked:bg-green-600"></div>
                    <span class="ms-3 text-sm font-medium text-gray-900 dark:text-gray-300">Remember me</span>
                  </label>
                <button type="button" class="text-white bg-green-700 hover:bg-green-800 focus:ring-4 focus:ring-green-300 font-medium rounded-lg text-sm px-5 py-2.5 mb-2 dark:bg-green-600 dark:hover:bg-green-700 focus:outline-none dark:focus:ring-green-800">Login</button>
            </form>
        </div>
        <!-- sidebar -->
        <div class="w-full bg-[url('/img/login.png')] flex justify-center items-center">
            <div class="flex gap-2">
                <NuxtImg class="object-contain w-24" src="/bpd.png" />
                <div class="flex flex-col text-white justify-center gap-1">
                    <h1 class="text-6xl font-bold">S-MEBB</h1>
                    <h2 class="italic">Service Mail Engine Bank BPD Bali</h2>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
const colorMode = useColorMode()

import { Tippy } from 'vue-tippy'
import 'tippy.js/dist/tippy.css'
</script>