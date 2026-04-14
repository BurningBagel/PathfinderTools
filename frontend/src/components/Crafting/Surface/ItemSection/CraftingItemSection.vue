<template>
    <!-- <CraftingButton :label="'dropdown type'"/> -->
     <BaseSelect class="crafting-button" :choices="itemTypeOptions" :title="'Item Type'"/>
     <span class="crafting-button">
        Item Level:
        <input class="text-shadow-lg/30" type="number" name="itemLevel" id="itemLevel" min="0" max="30" value="0" required>
     </span>
     <span class="crafting-button">
         <!-- <CraftingButton :label="'formula checkbox'"  @click="clickLog"/> -->
        Has formula?
        <input class="crafting-checkbox" type="checkbox" name="itemFormula" id="itemFormula">
     </span>
</template>
<!-- checkbox too high TODO  -->
 <!-- TODO change base button to receive input, or maybe make that base input after all? -->
<style>
.crafting-checkbox {
    appearance: none;
    width: 20px; height: 20px;
    background: #1A3A3A;
    border: 1px solid #2A5A55;
    border-radius: 3px;
    box-shadow: inset 0 1px 3px rgba(0,0,0,0.6);
    cursor: pointer;
    position: relative;
    flex-shrink: 0;
    transition: background 0.15s;
  }
  .crafting-checkbox:checked {
    background: #0A5A55;
    border-color: #50AAA5;
  }
  .crafting-checkbox:checked::after {
    content: '';
    position: absolute;
    left: 4px; top: 1px;
    width: 5px; height: 10px;
    border: 2px solid #C8840A;
    border-top: none; border-left: none;
    transform: rotate(45deg);
  }
  .crafting-checkbox:focus { outline: none; box-shadow: inset 0 1px 3px rgba(0,0,0,0.5), 0 0 0 2px rgba(0,180,160,0.25); }

</style>

<script setup lang="ts">
    import type { SelectData } from '../../../../models/selectData.model';
    import BaseSelect from '../../BaseSelect.vue';
    import CraftingButton from '../../CraftingButton.vue';
    
    let itemTypeOptions : SelectData[] = [{optionText:"Alchemical",optionValue:"alchemical"},{optionText:"Magical",optionValue:"magical"},{optionText:"Mundane",optionValue:"mundane"}]; // TODO placeholder

    function clickLog(){
        // console.log("I got clicked!")
    }

</script>