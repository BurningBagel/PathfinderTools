<template>
    <div class="flex flex-col">
        <!-- base with 3 slots, 1 extra + button to add more -->
         
        <FeatSlot v-for="slots in featsList"/>
        <CraftingButton :label="'+'" @onclick="addFeatSlot"/>
    </div>
</template>



<script setup lang="ts">
    import CraftingButton from '../../CraftingButton.vue';
    import FeatSlot from './FeatSlot.vue';
    

    const featsList : Object[] = [];

    function addFeatSlot(){
        featsList.push({});
    }


</script>