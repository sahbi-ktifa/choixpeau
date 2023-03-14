<script setup lang="ts">
import ChoixpeauVoice from "@/components/ChoixpeauVoice.vue";

interface Voice {
    label: string;
    sound: string;
}

const voices: Voice[] = [
    {label: 'Gryffondor', sound: '/voices/gryffondor.mp3'},
    {label: 'Serpentard', sound: '/voices/serpentard.mp3'},
    {label: 'Poufsouffle', sound: '/voices/Je-sais-Poufsouffle.mp3'},
    {label: 'Mais où te mettre', sound: '/voices/Mais-ou-te-mettre.mp3'},
    {label: 'Tu as d\'immense qualité', sound: '/voices/tu-as-dimmense-qualite.mp3'},
    {label: 'Pas à Serpentard', sound: '/voices/Pas-a-serpentard.mp3'},
    {label: 'Il y a des dons', sound: '/voices/Il-y-a-des-dons-oui.mp3'},
    {label: 'Difficile, beaucoup de courage', sound: '/voices/difficile-beaucoup-de-courage.mp3'},
]
</script>

<template>
  <div class="choixpeau">
      <choixpeau-voice v-for="voice in voices" :label="voice.label" :sound="voice.sound"/>
  </div>
</template>

<style scoped>

</style>
