<template>
    <button class="crafting-button"
    :class="{active,pressed}"
    @mousedown="pressed = true"
    @mouseup="pressed = false"
    @mouseleave="pressed = false"
    @click="$emit('click')"
    >
        {{ label }}
        <slot />
    </button>
</template>

<style lang="css" >
@import url('https://fonts.googleapis.com/css2?family=Inter:ital,opsz,wght@0,14..32,100..900;1,14..32,100..900&family=PT+Serif&display=swap');

.crafting-button{
  background-color: rgba(0,181,209,0.68);
  
  color: #f4b04f;
  font-family: "Inter" sans-serif;
  text-shadow: 0px 4px 4px black;
  padding: 10px 16px;
  border-radius: 6px;
  border: solid 9px #565656;
  box-shadow: 
  0 4px 0 #13443d,
  0 6px 8px rgba(0,0,0,0.4);
  transition: transform 0.05s ease, box-shadow 0.05s ease;
}

.crafting-button:active,
.crafting-button:pressed{
  transform: translateY(3px);
  box-shadow:
  0 1px 0 #13443d,
  0 2px 4px rgba(0,0,0,0.4);
}

</style>

<script setup lang="ts">

    import { ref } from 'vue'

    defineProps({
        active: Boolean,
        label: String
    })

    const pressed = ref(false)

</script>



<!--  https://pixabay.com/sound-effects/film-special-effects-steampunk-mechanical-gadget-188052/ sound effect -->

<!-- https://pixabay.com/sound-effects/film-special-effects-mechanical-push-switcher-393300/ -->

<!-- https://pixabay.com/sound-effects/film-special-effects-cassette-recorder-stop-button-mechanical-click-sound-359987/ -->