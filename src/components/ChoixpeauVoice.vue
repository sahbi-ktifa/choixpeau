<script setup lang="ts">
    import {computed} from "vue";

    const props = defineProps<{
        label: string,
        sound: string,
    }>()

    const soundSource = computed(() => props.sound + '.mp3')

</script>

<template>
    <div class="item">
        <h3>{{ label }}</h3>
        <audio controls>
            <source :src="soundSource" type="audio/mpeg" />
            Your browser does not support the audio element.
        </audio>
    </div>
</template>

<style scoped>
.item {
    padding-bottom: 5px;
    border-bottom: 1px dashed lightgray;
}

h3 {
    font-size: 1.2rem;
}

.item h3 {
    text-align: center;
    margin-bottom: 5px;
}

@media (min-width: 1024px) {
    .item h3 {
        text-align: left;
    }
}
</style>
