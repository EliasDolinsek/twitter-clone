<template>
    <div class="border-x" :class="twitterBorderColor">
        <div class="sticky top-0 px-4 bg-white/80 backdrop-blur-md dark:bg-dim-900/780">
            <h2 class="text-xl font-bold text-gray-800 dark:text-gray-100">{{ props.title }}</h2>
        </div>
        <div v-if="loading">Loading</div>
        <div v-else></div>
        <slot />
    </div>
</template>

<script setup>
const { twitterBorderColor } = useTailwindConfig()

const props = defineProps({
    title: {
        type: String,
        required: true
    },
    loading: {
        type: Boolean,
        default: false
    }
})
</script>