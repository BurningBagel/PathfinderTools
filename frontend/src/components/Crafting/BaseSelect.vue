<template>
    <select class="base-select" @change="onChange" :value="selectedValue">
        <option disabled value="">{{ title }}</option>
        <option v-for="(option,index) in testOptions" :index="index" :key="option.optionValue" :value="option.optionValue">
            {{ option.optionText }}</option>
    </select>
</template>

<style>
.base-select{
    text-shadow: 0px 4px 4px black;
    box-sizing: border-box;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    border-radius: 6px;
    /* border: solid 9px #565656; */
    cursor: pointer;
    transition: transform 0.05s ease, box-shadow 0.05s ease;
    box-shadow: 
        0 4px 0 #13443d,
        0 6px 8px rgba(0,0,0,0.4);
}
</style>

<script setup lang="ts">
import { SelectData } from '../../models/selectData.model';




defineProps(
    { selectedValue: String, testOptions: Array<SelectData>, title: String }
)

const emit = defineEmits(['update:selectedValue'])

function onChange(event: Event){
    const target = event.target as HTMLSelectElement;

    emit('update:selectedValue',target.value);
}

</script>