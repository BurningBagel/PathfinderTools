<script setup lang="ts">
import StartCraftButton from './StartCraftButton.vue';
import CraftingCharacterSection from './CharacterSection/CraftingCharacterSection.vue';
import CraftingFeatSection from './FeatSection/CraftingFeatSection.vue';
import CraftingItemSection from './ItemSection/CraftingItemSection.vue';




</script>

<template>
    <div class="bg flex flex-col">
        <div class="panel_bg">
            <div class="absolute rounded-full w-5 h-5 bg-gray-500 top-0.5 right-0.5" ></div>
            <div class="absolute rounded-full w-5 h-5 bg-gray-500 bottom-0.5 left-0.5" ></div>
            <div class="absolute rounded-full w-5 h-5 bg-gray-500 top-0.5 left-0.5" ></div>
            <div class="absolute rounded-full w-5 h-5 bg-gray-500 bottom-0.5 right-0.5" ></div>
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
                        <StartCraftButton class="basis-1/7"/>
                    </div>
                </div>
            </div>
    
        </div>
        <footer><a href="https://www.freepik.com/free-photo/flat-lay-rusty-metallic-surface_11684393.htm">Rust Texture by freepik</a></footer>
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

.panel_bg::after {
    content:"";
    position: absolute;
    inset: 0;
    background: url('/src/assets/flat-lay-rusty-metallic-surface.jpg');
    background-size: cover;
    background-position: center;

    opacity: 75%;
    mix-blend-mode: overlay;

    pointer-events: none;

}


.panel_bg {
    position: relative;
    display: flex;
    overflow: hidden;
    justify-content: center;
    align-items: center;
    min-width: 50vw;
    background: #B7410E;
    /* background: 
        url('/src/assets/flat-lay-rusty-metallic-surface.jpg'),
        linear-gradient(rgba(183,65,14,0.86),rgba(183,65,14,0.86)); */
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