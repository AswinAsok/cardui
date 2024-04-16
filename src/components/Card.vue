<template>
    <div class="cardContainer">
        <div class="imageContainer">
            <img src="/lessen.jpg" alt="" class="cardImage" />
        </div>
        <div class="cardTexts">
            <div class="mountainHeadingTexts">
                <p class="mountainText">Mountain</p>
                <div class="loveCircle">
                    <font-awesome-icon
                        :icon="['far', 'heart']"
                        style="color: #f04343"
                    />
                </div>
            </div>
            <p class="cardHeading">{{ mountain }}</p>
            <p class="cardContent">
                Lorem ipsum dolor sit amet consectetur, adipisicing elit.
                Voluptas, hic? Suscipit possimus. distinctio?
            </p>
            <p class="readMore">
                Read More
                <font-awesome-icon
                    :icon="['fas', 'arrow-right']"
                    style="color: #5f62f1"
                />
            </p>
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
.mountainHeadingTexts {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding-right: 1rem;
}

.loveCircle {
    -webkit-box-shadow: 0px 0px 15px -8px rgba(0, 0, 0, 0.91);
    -moz-box-shadow: 0px 0px 15px -8px rgba(0, 0, 0, 0.91);
    box-shadow: 0px 0px 15px -8px rgba(0, 0, 0, 0.91);

    width: 2rem;
    height: 2rem;

    display: flex;
    justify-content: center;
    align-items: center;

    border-radius: 15px;
}
.cardContainer {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;

    align-items: center;

    max-width: fit-content;
    width: 100%;

    -webkit-box-shadow: -1px 10px 18px 1px rgba(0, 0, 0, 0.22);
    -moz-box-shadow: -1px 10px 18px 1px rgba(0, 0, 0, 0.22);
    box-shadow: -1px 10px 18px 1px rgba(0, 0, 0, 0.22);

    border-radius: 15px;
}

@media (max-width: 792px) {
    .cardContainer {
        display: block;
    }
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

@media (max-width: 792px) {
    .cardImage {
        width: 100%;
    }
}

.cardTexts {
    padding: 1rem;
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
    margin-right: 1rem;
    color: #5f62f1;
    font-weight: 600;
}

.icon {
    margin-left: 0.5rem;
    font-size: 1.5rem;
    color: #2aacea;
    transition: all 0.3s;
}
</style>
