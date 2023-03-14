<script setup lang="ts">
import ChoixpeauVoice from "@/components/ChoixpeauVoice.vue";

interface Voice {
    label: string;
    sound: string;
}

const voices: Voice[] = [
    {label: 'Gryffondor', sound: '/src/assets/voices/gryffondor.mp3'},
    {label: 'Serpentard', sound: '/src/assets/voices/serpentard.mp3'},
    {label: 'Poufsouffle', sound: '/src/assets/voices/Je-sais-Poufsouffle.mp3'},
    {label: 'Mais où te mettre', sound: '/src/assets/voices/Mais-ou-te-mettre.mp3'},
    {label: 'Tu as d\'immense qualité', sound: '/src/assets/voices/tu-as-dimmense-qualite.mp3'},
    {label: 'Pas à Serpentard', sound: '/src/assets/voices/Pas-a-serpentard.mp3'},
    {label: 'Il y a des dons', sound: '/src/assets/voices/Il-y-a-des-dons-oui.mp3'},
    {label: 'Difficile, beaucoup de courage', sound: '/src/assets/voices/difficile-beaucoup-de-courage.mp3'},
]
</script>

<template>
  <div class="choixpeau">
      <choixpeau-voice v-for="voice in voices" :label="voice.label" :sound="voice.sound"/>
  </div>
</template>

<style scoped>

</style>
