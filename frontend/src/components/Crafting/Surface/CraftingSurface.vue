<script setup lang="ts">
import CraftingCharacterSection from './CharacterSection/CraftingCharacterSection.vue';
import CraftingFeatSection from './FeatSection/CraftingFeatSection.vue';
import CraftingItemSection from './ItemSection/CraftingItemSection.vue';

</script>

<template>
    <div class="bg">
        <div class="fg">
            <div class="panel">
                <CraftingCharacterSection />
                <CraftingItemSection />
                <CraftingFeatSection />
            </div>
    
        </div>
        <footer><a href="https://www.freepik.com/free-photo/flat-lay-rusty-metallic-surface_11684393.htm">Image by freepik</a></footer>
    </div>
</template>

<style lang="css" scoped>
.bg {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100vw;
    height: 100vh;
    background-color: #F0E7D8;
}



.fg {
    display: flex;
    justify-content: center;
    align-items: center;
    position: absolute;
    height: 70%;
    width: 50%;
    background: 
    linear-gradient(rgba(183,65,14,0.86),rgba(183,65,14,0.86)),
    url('/src/assets/flat-lay-rusty-metallic-surface.jpg');

    background-size: cover;
    background-position: center;

    background-blend-mode: multiply;
    border-width: 5px;
    border-radius: 5px;
    box-shadow: 4px 4px 4px #000000,
                 2px 2px 7px #9C370B inset;

    /* fill: #B7410E; */
    /* fill-opacity: 86%; */
    stroke: #9C370B;
    stroke-width: 10;
}
/* <a href="https://www.freepik.com/free-photo/flat-lay-rusty-metallic-surface_11684393.htm">Image by freepik</a> */
.panel {
    position: absolute;
    x: 10;
    y: 12;
    stroke: red;
}


</style>