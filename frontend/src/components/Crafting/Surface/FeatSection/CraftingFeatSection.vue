<script setup lang="ts">
import CraftingButton from '../../CraftingButton.vue';
import FeatSlot from './FeatSlot.vue';

</script>

<template>
    <div class="flex flex-col">
        <!-- base with 3 slots, 1 extra + button to add more -->
        <FeatSlot />
        <CraftingButton :label="'+'" />
    </div>
</template>