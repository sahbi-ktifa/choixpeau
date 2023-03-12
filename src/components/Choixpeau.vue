<script setup lang="ts">
import ChoixpeauVoice from "@/components/ChoixpeauVoice.vue";

interface Voice {
    label: string;
    sound: string;
}

const voices: Voice[] = [
    {label: 'Gryffondor', sound: 'gryffondor'},
    {label: 'Serpentard', sound: 'serpentard'},
]
</script>

<template>
  <div class="choixpeau">
      <choixpeau-voice v-for="voice in voices" :label="voice.label" :sound="voice.sound"/>
  </div>
</template>

<style scoped>

</style>
