<template>
    <!-- <CraftingButton :label="'dropdown type'"/> -->
     <BaseSelect :options="itemTypeOptions" :title="'Dropdown Type'"/>
    <CraftingButton :label="'item level'" />
    <CraftingButton :label="'formula checkbox'"  @click="clickLog"/>
</template>





<script setup lang="ts">
    import type { SelectData } from '../../../../models/selectData.model';
    import BaseSelect from '../../BaseSelect.vue';
    import CraftingButton from '../../CraftingButton.vue';
    
    let itemTypeOptions : SelectData[] = [];

    function clickLog(){
        // console.log("I got clicked!")
    }

</script>