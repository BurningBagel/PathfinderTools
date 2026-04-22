<template>
  <div class="relative">
    <div
      class="bg-red-800 absolute w-5 h-5 top-0.5 right-0.5 rounded-full flex items-center justify-center border border-red-400 text-red-200 text-xs font-bold leading-none cursor-pointer"
      @click="$emit('remove')"
    >X</div>
    <BaseSelect :title="'Choose a Feat'" :choices="featChoices" />
  </div>
</template>

<style scoped lang="css"></style>

<script setup lang="ts">
import type { SelectData } from "../../../../models/selectData.model";
import BaseSelect from "../../BaseSelect.vue";

let featChoices: SelectData[] = [
  //TODO replace with global constants
  {
    optionText: "Junk Tinker",
    optionValue: "junk_tinker",
  },
  {
    optionText: "Specialty Crafting",
    optionValue: "spec_crafting",
  },
];
</script>
