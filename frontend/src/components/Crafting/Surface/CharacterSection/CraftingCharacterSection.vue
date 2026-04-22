<template>
    <!-- <CraftingButton :label="'proficiency'" class="button" /> -->
    <BaseSelect class="crafting-button" :title="'Proficiency'" :choices="proficiencyChoices"/>
    <!-- <CraftingButton :label="'char level'" class="button" /> -->
     <span class="crafting-button">
    Character Level:
    <input
      class="text-shadow-lg/30"
      type="number"
      name="charLevel"
      id="charLevel"
      min="1"
      max="20"
      value="1"
      required
    />
  </span>
    <!-- <CraftingButton :label="'circum. bonuses'" class="button" /> -->
     <span class="crafting-button">
    Bonuses:
    <input
      class="text-shadow-lg/30"
      type="number"
      name="bonuses"
      id="bonuses"
      min="-10"
      max="10"
      value="0"
      required
    />
  </span>
</template>

<style lang="css" scoped>
.button{
    position: relative;
}
</style>


<script setup lang="ts">
import type { SelectData } from '../../../../models/selectData.model';
import BaseSelect from '../../BaseSelect.vue';

let proficiencyChoices : SelectData[] = [ //TODO replace with global constants
    {
        optionText:"Trained",
        optionValue:"trained"
    },
    {
        optionText:"Expert",
        optionValue:"expert"
    },
]

</script>