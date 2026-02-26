<script setup lang="ts">
import CraftingCharacterSection from './CharacterSection/CraftingCharacterSection.vue';
import CraftingFeatSection from './FeatSection/CraftingFeatSection.vue';
import CraftingItemSection from './ItemSection/CraftingItemSection.vue';

</script>

<template>
    <div class="bg">
        <img src="..\..\..\assets\flat-lay-rusty-metallic-surface.jpg" alt="">
        <div class="fg">
            <CraftingCharacterSection />
            <CraftingItemSection />
            <CraftingFeatSection />
        </div>

    </div>
    <a href="https://www.freepik.com/free-photo/flat-lay-rusty-metallic-surface_11684393.htm">Image by freepik</a>
</template>

<style lang="css" scoped>
.bg {
    fill: #B7410E;
    fill-opacity: 86%;
    border-radius: 5px;
    stroke: #9C370B;
    stroke-width: 10;
    box-shadow: 4px 4px 4px #000000,
                 2px 2px 7px #9C370B inset;
}
/* <a href="https://www.freepik.com/free-photo/flat-lay-rusty-metallic-surface_11684393.htm">Image by freepik</a> */
.fg {
    position: absolute;
    x: 10;
    y: 12;
}

img {
    position: absolute;
    x: 0;
    y: 0;

    width: 100%;
    height: 100%;

    background-color: rgba(0,0,0,0.6);
}

</style>