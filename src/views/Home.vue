<script setup>
import { ref } from 'vue'

defineProps({
  msg: String
})

const count = ref(0)
</script>

<template>
    <div class="flex justify-center items-center flex-col mt-[20rem]">
        <h1 class="font-bold text-4xl">{{ message }}</h1>

        <p class="font-normal mt-2 text-lg">
            {{ description }}
        </p>
        <div class="grid grid-cols-3 gap-8 mt-12">
            <div id="tailwindcss">
                <img class="w-32" src="https://seeklogo.com/images/T/tailwind-css-logo-5AD4175897-seeklogo.com.png" alt="Tailwind CSS" />
            </div>
            <div id="vue">
                <img class="w-24" src="https://vuejs.org/images/logo.png" alt="Vue.js" />
            </div>
            <div id="volar">
                <img class="w-24" src="https://camo.githubusercontent.com/61e102d7c605ff91efedb9d7e47c1c4a07cef59d3e1da202fd74f4772122ca4e/68747470733a2f2f766974656a732e6465762f6c6f676f2e737667" alt="Lite" />
            </div>
        </div>

        <button class="p-4 bg-slate-700 text-white mt-4 rounded-lg" type="button" @click="count++">count is {{ count }}</button>

        <!-- change message by input then clicked the button -->
        <label class="mt-4" for="message">Change title :</label>
        <input type="text" v-model="message" class="border border-slate-700 p-2 rounded-md"/>
    </div>
</template>

<script>
    export default {
        name: 'Home',
        data() {
            return {
                message: 'Welcome',
                description: 'This is Vue.js project use Tailwind CSS and Vite'
            }
        }
    }
</script>