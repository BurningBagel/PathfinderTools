<script setup lang="ts">
import CraftingCharacterSection from './CharacterSection/CraftingCharacterSection.vue';
import CraftingFeatSection from './FeatSection/CraftingFeatSection.vue';
import CraftingItemSection from './ItemSection/CraftingItemSection.vue';

</script>

<template>
    <div class="bg">
        <div class="fg">
            <CraftingCharacterSection />
            <CraftingItemSection />
            <CraftingFeatSection />
        </div>

    </div>
    <footer><a href="https://www.freepik.com/free-photo/flat-lay-rusty-metallic-surface_11684393.htm">Image by freepik</a></footer>
</template>

<style lang="css" scoped>
.bg {
    position: relative;
    background: 
    url('@/assets/flat-lay-rusty-metallic-surface.jpg'),
    linear-gradient(#B7410E,#B7410E);

    background-size: cover;
    background-position: center;

    background-blend-mode: multiply;
    border-radius: 5px;
    box-shadow: 4px 4px 4px #000000,
                 2px 2px 7px #9C370B inset;

    /* fill: #B7410E; */
    /* fill-opacity: 86%; */
    stroke: #9C370B;
    stroke-width: 10;
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