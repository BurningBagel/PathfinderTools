<template>
    <!-- <CraftingButton :label="'dropdown type'"/> -->
     <BaseSelect class="crafting-button" :choices="itemTypeOptions" :title="'Item Type'"/>
    <CraftingButton :label="'item level'" />
    <CraftingButton :label="'formula checkbox'"  @click="clickLog"/>
</template>





<script setup lang="ts">
    import type { SelectData } from '../../../../models/selectData.model';
    import BaseSelect from '../../BaseSelect.vue';
    import CraftingButton from '../../CraftingButton.vue';
    
    let itemTypeOptions : SelectData[] = [{optionText:"Alchemical",optionValue:"alchemical"},{optionText:"Magical",optionValue:"magical"}]; // TODO placeholder

    function clickLog(){
        // console.log("I got clicked!")
    }

</script>