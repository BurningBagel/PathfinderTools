<template>
     <button class="crafting-button"
    :class="{active,pressed}"
    @mousedown="pressed = true"
    @mouseup="pressed = false"
    @mouseleave="pressed = false"
    @click="$emit('click')"
    >
        {{ label }}
        <slot />
    </button>
</template>

<script setup lang="ts">


    defineProps({
        active: Boolean,
        label: String,
        pressed: Boolean
    })


</script>