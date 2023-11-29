<script>
export default {
    name: "SecondSection",
    data() {
        return {
            iconsContainer: [
                {
                    srcIcon: "/src/assets/img/buy-comics-digital-comics.png",
                    titleIcon: "DIGITAL COMICS"
                },
                {
                    srcIcon: "/src/assets/img/buy-comics-merchandise.png",
                    titleIcon: "DC MERCHANDISE"
                },
                {
                    srcIcon: "/src/assets/img/buy-comics-subscriptions.png",
                    titleIcon: "SUBSCRIPTION"
                },
                {
                    srcIcon: "/src/assets/img/buy-comics-shop-locator.png",
                    titleIcon: "COMIC SHOP LOCATOR"
                },
                {
                    srcIcon: "/src/assets/img/buy-dc-power-visa.svg",
                    titleIcon: "DC POWER VISA"
                }
            ]
        }
    }
}
</script>

<template>
    <section>
        <div>
            <div class="iconContainer" v-for="iconContainer in iconsContainer">
                <img :src="iconContainer.srcIcon" :alt="iconContainer.titleIcon">
                <div>{{ iconContainer.titleIcon }}</div>
            </div>
        </div>
    </section>
</template>

<style scoped>
section {
    height: 150px;
    background-color: rgba(2, 130, 249, 255);
    display: flex;
    justify-content: center;
}

section>div {
    height: 100%;
    width: 70%;
    padding: 0 1rem;
    display: flex;
}

.iconContainer {
    height: 100%;
    width: 20%;
    padding: 3rem 0;
    display: flex;
    align-items: center;
    justify-content: center;
}

.iconContainer>img {
    height: 100%;
}

.iconContainer>div {
    margin-left: 0.5rem;
    font-size: 0.6rem;
    color: white;
}

.iconContainer:last-of-type>img {
    height: 75%;
}
</style>