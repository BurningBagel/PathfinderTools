<template>
    <div class="flex flex-col">
        <!-- base with 3 slots, 1 extra + button to add more -->
         
        <FeatSlot v-for="(slot,index) in featsList" :key="slot.id" :index="index" @remove="removeFeatSlot(index)"/>
        <CraftingButton :label="'+'" @onclick="addFeatSlot"/>
    </div>
</template>



<script setup lang="ts">
    import { reactive } from 'vue';
    import CraftingButton from '../../CraftingButton.vue';
    import FeatSlot from './FeatSlot.vue';
    

    const featsList : {"id":number,"text":String}[] = reactive([]);
    var indexCounter : number = 0;

    function addFeatSlot(){
        featsList.push({"id":indexCounter,"text":"text"});
        indexCounter++;
    }

    function removeFeatSlot(indexToRemove:number){
        featsList.splice(indexToRemove,1);
    }



</script>