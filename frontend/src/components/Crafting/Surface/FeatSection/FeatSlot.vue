<script setup lang="ts">
import CraftingButton from '../../CraftingButton.vue';

</script>

<template>
    <div class="relative">
        <div class="bg-red-500 absolute w-5 h-5 top-0.5 right-0.5 rounded-full" @click="$emit('remove')"></div>
        <CraftingButton :label="'Feat Slot'"/>
    </div>
</template>


<style scoped lang="css">


</style>