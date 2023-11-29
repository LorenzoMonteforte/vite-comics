<script>
export default {
    name: "CardContainer",
    props: {
        srcCard: String,
        titleCard: String
    }
}
</script>

<template>
    <div class="cardContainer">
        <img :src="srcCard" :alt="titleCard">
        <div>{{ titleCard }}</div>
    </div>
</template>

<style scoped>
.cardContainer {
    width: calc(100% / 6);
    padding: 0 0.5rem;
}

.cardContainer>img {
    width: 100%;
    aspect-ratio: 1;
    object-fit: cover;
    object-position: top;
    display: block;
}

.cardContainer>div {
    margin-top: 0.5rem;
    font-size: 0.6rem;
    color: white;
}

.cardContainer:nth-child(1n + 8) {
    margin-top: 2rem;
}
</style>