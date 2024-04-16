<template>
    <div class="cardContainer">
        <div class="imageContainer">
            <img src="/lessen.jpg" alt="" class="cardImage" />
        </div>
        <div class="cardTexts">
            <p class="mountainText">Mountain</p>
            <p class="cardHeading">{{ mountain }}</p>
            <p class="cardContent">
                Lorem ipsum dolor sit amet consectetur, adipisicing elit.
                Voluptas, hic? Suscipit possimus. distinctio?
            </p>
            <p class="readMore">Read More</p>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        mountain: {
            type: String,
            required: true,
        },
    },
};
</script>

<style scoped>
.cardContainer {
    display: flex;
    flex-direction: row;
    column-gap: 1rem;
    align-items: center;

    -webkit-box-shadow: -1px 10px 18px 1px rgba(0, 0, 0, 0.22);
    -moz-box-shadow: -1px 10px 18px 1px rgba(0, 0, 0, 0.22);
    box-shadow: -1px 10px 18px 1px rgba(0, 0, 0, 0.22);

    border-radius: 15px;
}

.imageContainer {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 0.75rem;
}

.cardImage {
    width: 22rem;
    height: 15rem;
    border-radius: 15px;
}

.cardTexts {
    display: flex;
    flex-direction: column;
    font-family: "Montserrat", sans-serif;
}

.mountainText {
    color: #2aacea;
    font-family: "Yellowtail", sans-serif;
    font-size: 1.5rem;
}

.cardHeading {
    margin-top: 0.5rem;
    font-weight: 600;
    font-size: 1.5rem;
}

.cardContent {
    margin-top: 0.5rem;
    max-width: 20rem;
    font-size: 0.9rem;
    line-height: 1.25rem;
}

.readMore {
    margin-top: 1rem;
    text-align: right;
    margin-right: 2rem;
}

.icon {
    margin-left: 0.5rem;
    font-size: 1.5rem;
    color: #2aacea;
    transition: all 0.3s;
}
</style>
