<script setup lang="ts">
import CraftingButton from '../../CraftingButton.vue';

</script>

<template>
    <CraftingButton :label="'proficiency'" class="button" style="top: 75px;"/>
    <CraftingButton :label="'char level'" class="button" style="left: 100px"/>
    <CraftingButton :label="'circum. bonuses'" class="button" style="left: 200px"/>
</template>

<style lang="css" scoped>
.button{
    position: relative;
}


</style>