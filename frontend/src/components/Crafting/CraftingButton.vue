<template>
    <BaseButton class="crafting-button" @click="onclick">
    {{ label }}
    </BaseButton>
</template>

<style lang="css" >
@import url('https://fonts.googleapis.com/css2?family=Inter:ital,opsz,wght@0,14..32,100..900;1,14..32,100..900&family=PT+Serif&display=swap');

.crafting-button{
  color: #D59C4B;
  font-family: "Inter" sans-serif;
  font-size: 36;
  text-shadow: 0px 4px 4px black;
  text-align: center;
  padding: 5px 10px;
}

.crafting-button:active,
.crafting-button:pressed{
  transform: translateY(3px);
  box-shadow:
  0 1px 0 #13443d,
  0 2px 4px rgba(0,0,0,0.4);
}

.crafting-button:before,
.crafting-button:after {
  content: attr(title);
  padding: 5px;
  color: rgba(255, 255, 255, .1);
}

.crafting-button:before {
  top: 1px;
  left: 1px
}

.crafting-button:after {
  top: 2px;
  left: 2px
}

</style>

<script setup lang="ts">

    import BaseButton from './BaseButton.vue';

    defineProps({
        active: Boolean,
        label: String,
        onclick: Function
    })



</script>



<!--  https://pixabay.com/sound-effects/film-special-effects-steampunk-mechanical-gadget-188052/ sound effect -->

<!-- https://pixabay.com/sound-effects/film-special-effects-mechanical-push-switcher-393300/ -->

<!-- https://pixabay.com/sound-effects/film-special-effects-cassette-recorder-stop-button-mechanical-click-sound-359987/ -->