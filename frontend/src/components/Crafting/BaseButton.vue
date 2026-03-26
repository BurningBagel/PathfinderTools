<template>
     <button
    v-bind="$attrs" 
    :class="['base-button',$attrs.class,{'is-pressed':pressed,'is-active':active}]"
    @mousedown="pressed = true"
    @mouseup="pressed = false"
    @mouseleave="pressed = false"
    @click="$emit('click')"
    >
        <slot />
    </button>
</template>

<style lang="css">
.base-button{
    background-color: rgba(0,181,209,0.68);
    border-radius: 6px;
    border: solid 9px #565656;
    transition: transform 0.05s ease, box-shadow 0.05s ease;
    box-shadow: 
        0 4px 0 #13443d,
        0 6px 8px rgba(0,0,0,0.4);
}


</style>

<script setup lang="ts">
    import { ref } from 'vue';

    defineProps({
        active: Boolean
    })

    const pressed = ref(false)
</script>