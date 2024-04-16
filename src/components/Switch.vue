<script>
export default {
    props: {
        customFunction: {
            type: Function,
            required: true,
        },
    },
    methods: {
        handleClick(mountain) {
            this.customFunction(mountain);
            console.log(mountain);
        },
    },
};
</script>

<template>
    <div class="switchContainer">
        <div @click="handleClick('Lessen Peak')" class="switch">
            Lessen Peak
        </div>
        <div @click="handleClick('Mount Shasta')" class="switch">
            Mount Shasta
        </div>
        <div @click="handleClick('Eureka Peak')" class="switch">
            Eureka Peak
        </div>
    </div>
</template>

<style scoped>
.switchContainer {
    display: flex;
    justify-content: center;
    gap: 1rem;
    background-color: #e2e8f0;
    padding: 0.5rem;
    border-radius: 30px;
    margin-bottom: 2rem;
}

.switch {
    padding: 0.5rem 1rem;
    font-size: 0.9rem;
    border-radius: 15px;
    background-color: #ffffff;
    color: #000000;
    font-family: "Montserrat", sans-serif;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.3s;
}
</style>
