<template>
    <button class="crafting-button"
    :class="{active,pressed}"
    @mousedown="pressed = true"
    @mouseup="pressed = false"
    @mouseleave="pressed = false"
    @click="$emit('click')"
    >
        <slot />
    </button>
</template>

<script setup lang="ts">

    import { ref } from 'vue'

    defineProps({
        active: Boolean
    })

    const pressed = ref(false)

</script>



<!--  https://pixabay.com/sound-effects/film-special-effects-steampunk-mechanical-gadget-188052/ sound effect -->

<!-- https://pixabay.com/sound-effects/film-special-effects-mechanical-push-switcher-393300/ -->

<!-- https://pixabay.com/sound-effects/film-special-effects-cassette-recorder-stop-button-mechanical-click-sound-359987/ -->