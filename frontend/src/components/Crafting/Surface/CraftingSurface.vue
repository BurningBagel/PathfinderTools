<script setup lang="ts">
import StartCraftButton from '../StartCraftButton.vue';
import CraftingCharacterSection from './CharacterSection/CraftingCharacterSection.vue';
import CraftingFeatSection from './FeatSection/CraftingFeatSection.vue';
import CraftingItemSection from './ItemSection/CraftingItemSection.vue';

//TODO: BOLTS

//TODO: FEATS LIST

//TODO: CRAFT BUTTON

//TODO: RUST EFFECT ON BUTTONS AND BOLTS

</script>

<template>
    <div class="bg flex flex-col">
        <div class="panel_bg">
            <div class="panel my-4">
                <div class="panel_fg">
                    <div class="flex gap-4 justify-between mx-15 my-15" >
                        <CraftingItemSection />
                    </div>
                    <div class="flex gap-4 justify-between mx-15 my-15">
                        <CraftingCharacterSection />
                    </div>
                    <div class="flex flex-row justify-between mx-15 my-5">
                        <CraftingFeatSection />
                        <StartCraftButton />
                    </div>
                </div>
            </div>
    
        </div>
        <footer><a href="https://www.freepik.com/free-photo/flat-lay-rusty-metallic-surface_11684393.htm">Image by freepik</a></footer>
    </div>
</template>

<style lang="css">
.section{
    display: flex;
    flex-direction: row;
    flex-shrink: 3;
}


.bg {
    margin: 0%;
    display: flex;
    justify-content: center;
    align-items: center;
    min-width: 100vw;
    min-height: 100vh;
    margin: 0;
    padding: 0;
    background-color: #F0E7D8;
}


.panel_bg {
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 70vh;
    min-width: 50vw;
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
    
    
    min-height: 95%;
    min-width: 95%;

    border: #000000 1px solid;
    border-radius: 5px;
    box-shadow: 0px 4px 4px #000000 inset;
}

.panel_fg{
    display: flex;
    flex-direction: column;
}


</style>