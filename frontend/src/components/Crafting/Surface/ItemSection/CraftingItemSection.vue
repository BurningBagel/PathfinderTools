<template>
    <CraftingButton :label="'dropdown type'"/>
    <CraftingButton :label="'item level'" />
    <CraftingButton :label="'formula checkbox'"  @click="clickLog"/>
</template>





<script setup lang="ts">
    import CraftingButton from '../../CraftingButton.vue';
    
    
    function clickLog(){
        // console.log("I got clicked!")
    }

</script>