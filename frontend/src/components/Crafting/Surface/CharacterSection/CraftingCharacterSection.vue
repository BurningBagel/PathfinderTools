<script setup lang="ts">
import CraftingButton from '../../CraftingButton.vue';

</script>

<template>
    <CraftingButton :label="'proficiency'" class="button" />
    <CraftingButton :label="'char level'" class="button" />
    <CraftingButton :label="'circum. bonuses'" class="button" />
</template>

<style lang="css" scoped>
.button{
    position: relative;
}


</style>