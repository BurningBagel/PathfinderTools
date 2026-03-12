<script setup lang="ts">
import CraftingCharacterSection from './CharacterSection/CraftingCharacterSection.vue';
import CraftingFeatSection from './FeatSection/CraftingFeatSection.vue';
import CraftingItemSection from './ItemSection/CraftingItemSection.vue';

</script>

<template>
    <div class="bg">
        <div class="panel_bg">
            <div class="panel">
                <div class="panel_fg">
                    <CraftingCharacterSection />
                    <CraftingItemSection />
                    <CraftingFeatSection />
                </div>
            </div>
    
        </div>
        <footer><a href="https://www.freepik.com/free-photo/flat-lay-rusty-metallic-surface_11684393.htm">Image by freepik</a></footer>
    </div>
</template>

<style lang="css">
.bg {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100vw;
    height: 100vh;
    background-color: #F0E7D8;
}



.panel_bg {
    display: flex;
    justify-content: center;
    align-items: center;
    position: absolute;
    height: 70%;
    width: 50%;
    /* background: #B7410E; */
    background: 
        url('/src/assets/flat-lay-rusty-metallic-surface.jpg'),
        linear-gradient(rgba(183,65,14,0.86),rgba(183,65,14,0.86));
    background-size: cover;
    background-position: center;
    background-blend-mode: overlay;

    
    box-shadow: 4px 4px 4px #000000,
    2px 2px 7px #9C370B inset;
    
    /* fill: #B7410E; */
    /* fill-opacity: 86%; */
    border: 10px solid #9C370B;
    border-radius: 5px;
}
/* <a href="https://www.freepik.com/free-photo/flat-lay-rusty-metallic-surface_11684393.htm">Image by freepik</a> */
.panel {
    
    position: absolute;
    
    height: 95%;
    width: 95%;

    border: #000000 1px solid;
    border-radius: 5px;
    box-shadow: 0px 4px 4px #000000 inset;

    x: 10;
    y: 12;
    stroke: red;
}


</style>