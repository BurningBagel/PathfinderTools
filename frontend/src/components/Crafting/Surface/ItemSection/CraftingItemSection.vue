<template>
    <!-- <CraftingButton :label="'dropdown type'"/> -->
     <BaseSelect class="crafting-button" :choices="itemTypeOptions" :title="'Item Type'"/>
     <input class="crafting-button" type="number" name="itemLevel" id="itemLevel" min="0" max="30" value="0" required>
    <CraftingButton :label="'formula checkbox'"  @click="clickLog"/>
</template>



<script setup lang="ts">
    import type { SelectData } from '../../../../models/selectData.model';
    import BaseSelect from '../../BaseSelect.vue';
    import CraftingButton from '../../CraftingButton.vue';
    
    let itemTypeOptions : SelectData[] = [{optionText:"Alchemical",optionValue:"alchemical"},{optionText:"Magical",optionValue:"magical"},{optionText:"Mundane",optionValue:"mundane"}]; // TODO placeholder

    function clickLog(){
        // console.log("I got clicked!")
    }

</script>