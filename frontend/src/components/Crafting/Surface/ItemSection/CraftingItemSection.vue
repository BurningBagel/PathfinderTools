<template>
  <!-- <CraftingButton :label="'dropdown type'"/> -->
  <BaseSelect
    class="crafting-button"
    :choices="itemTypeOptions"
    :title="'Item Type'"
  />
  <span class="crafting-button">
    Item Level:
    <input
      class="text-shadow-lg/30"
      type="number"
      name="itemLevel"
      id="itemLevel"
      min="0"
      max="30"
      value="0"
      required
    />
  </span>
  <span class="crafting-button">
    <!-- <CraftingButton :label="'formula checkbox'"  @click="clickLog"/> -->
    Has formula?
    <label class="checkbox-wrapper">
      <input
        class="crafting-checkbox"
        type="checkbox"
        name="itemFormula"
        id="itemFormula"
      />
    </label>
  </span>
</template>
<!-- checkbox too high TODO  -->
<!-- TODO change base button to receive input, or maybe make that base input after all? -->
<style>

.checkbox-wrapper{
  display: inline-block;
  vertical-align: middle;
  width: 20px;
  height: 20px;
  position: relative;
  flex-shrink: 0;
}


.crafting-checkbox {
  appearance: none;
  -webkit-appearance: none;
  width: 100%;
  height: 100%;
  background: #1a3a3a;
  border: 1px solid #2a5a55;
  border-radius: 3px;
  box-shadow: inset 0 1px 3px rgba(0, 0, 0, 0.6);
  cursor: pointer;
  display: block;
  transition: background 0.15s;
}
.crafting-checkbox:checked {
  background: #0a5a55;
  border-color: #50aaa5;
}
.checkbox-wrapper:has(.crafting-checkbox:checked)::after {
  content: "";
  position: absolute;
  left: 5px;
  top: 2px;
  width: 6px;
  height: 11px;
  border: 2px solid #c8840a;
  border-top: none;
  border-left: none;
  transform: rotate(45deg);
  pointer-events: none;
}
.crafting-checkbox:focus {
  outline: none;
  box-shadow:
    inset 0 1px 3px rgba(0, 0, 0, 0.5),
    0 0 0 2px rgba(0, 180, 160, 0.25);
}
</style>

<script setup lang="ts">
import type { SelectData } from "../../../../models/selectData.model";
import BaseSelect from "../../BaseSelect.vue";

let itemTypeOptions: SelectData[] = [
  { optionText: "Alchemical", optionValue: "alchemical" },
  { optionText: "Magical", optionValue: "magical" },
  { optionText: "Mundane", optionValue: "mundane" },
  // { optionText: "REALLYBIGNAMETHATSSOBIGOMGWTFBBQ", optionValue: "big"},
]; // TODO placeholder

function clickLog() {
  // console.log("I got clicked!")
}
</script>
