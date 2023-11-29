<script>
export default {
    name: "ThirdComponent",
    data() {
        return {
            allInformations: [
                {
                    title: "DC COMICS",
                    informations: [
                        "Characters",
                        "Comics",
                        "Movies",
                        "TV",
                        "Games",
                        "Videos",
                        "News"
                    ]
                },
                {
                    title: "SHOP",
                    informations: [
                        "Shop DC",
                        "Shop DC Collectibles"
                    ]
                },
                {
                    title: "DC",
                    informations: [
                        "Terms Of Use",
                        "Privacy policy (New)",
                        "Ad Choices",
                        "Advertising",
                        "Jobs",
                        "Subscriptions",
                        "Talent Workshop",
                        "CPSC Certificates",
                        "Ratings",
                        "Shop Help",
                        "Contact Us"
                    ]
                },
                {
                    title: "SITES",
                    informations: [
                        "DC",
                        "MAD Magazine",
                        "DC Kids",
                        "DC Universe",
                        "DC Power Visa"
                    ]
                },
            ]
        }
    }
}
</script>

<template>
    <section>
        <div>
            <div id="infoContainer">
                <div>
                    <h5>{{ allInformations[0].title }}</h5>
                    <ul>
                        <li v-for="info in allInformations[0].informations">{{ info }}</li>
                    </ul>
                    <h5>{{ allInformations[1].title }}</h5>
                    <ul>
                        <li v-for="info in allInformations[1].informations">{{ info }}</li>
                    </ul>
                </div>
                <div>
                    <h5>{{ allInformations[2].title }}</h5>
                    <ul>
                        <li v-for="info in allInformations[2].informations">{{ info }}</li>
                    </ul>
                </div>
                <div>
                    <h5>{{ allInformations[3].title }}</h5>
                    <ul>
                        <li v-for="info in allInformations[3].informations">{{ info }}</li>
                    </ul>
                </div>
            </div>
            <div id="dcImageContainer"></div>
        </div>
    </section>
</template>

<style scoped>
section {
    display: flex;
    justify-content: center;
    background-image: url("../assets/img/footer-bg.jpg");
}

section>div {
    width: 70%;
    display: flex;
    justify-content: space-between;
}

#infoContainer {
    width: calc(100% / 3);
    display: flex;
}

#infoContainer>div {
    width: calc(100% / 3);
    padding: 2rem 0.5rem;
}

#infoContainer>div>ul {
    margin-top: 0.5rem;
}

#infoContainer>div>ul>li {
    font-size: 0.7rem;
    color: grey;
}

#infoContainer>div>h5 {
    margin-top: 1rem;
    color: white;
}

#infoContainer>div>h5:first-of-type {
    margin-top: 0;
}

#dcImageContainer {
    height: 100%;
    aspect-ratio: 16 / 9;
    background-image: url("../assets/img/dc-logo-bg.png");
    background-size: cover;
    background-position: 50%;
}
</style>