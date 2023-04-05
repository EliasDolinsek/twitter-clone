<template>
<div class="p-3 hover:bg-gray-100 dark:bg-dim-300 border-b" :class="wrapperClasses">
    <slot />
</div>
</template>

<script setup>
const {defaultTransition, twitterBorderColor} = useTailwindConfig()

const wrapperClasses = computed(() => `${defaultTransition} ${twitterBorderColor}`)
</script>