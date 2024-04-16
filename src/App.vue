<script setup>
import Switch from "./components/Switch.vue";
import Card from "./components/Card.vue";
import { ref } from "vue";
</script>

<script>
import Card from "./components/Card.vue";
const currentMountain = ref("Lessen Peak");

export default {
    components: {
        Card,
    },
    props: {
        mountain: {
            type: String,
            required: true,
        },
    },
    methods: {
        updateMountain(mountain) {
            currentMountain.value = mountain;
        },
    },
};
</script>

<template>
    <div class="backgroundContainer">
        <Switch :customFunction="updateMountain" :mountain="currentMountain"/>
        <Card :mountain="currentMountain" />
    </div>
</template>

<style scoped>
.backgroundContainer {
    max-width: 100vw;
    min-height: 100vh;
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
}
</style>
