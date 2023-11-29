<script>
export default {
    name: "FooterComponent",
    data() {
        return {
            socialLogo: [
                {
                    nameSocialLogo: "Facebook",
                    srcSocialLogo: "img/footer-facebook.png"
                },
                {
                    nameSocialLogo: "Twitter",
                    srcSocialLogo: "img/footer-twitter.png"
                },
                {
                    nameSocialLogo: "You Tube",
                    srcSocialLogo: "img/footer-youtube.png"
                },
                {
                    nameSocialLogo: "Pinterest",
                    srcSocialLogo: "img/footer-pinterest.png"
                },
                {
                    nameSocialLogo: "Periscope",
                    srcSocialLogo: "img/footer-periscope.png"
                }
            ]
        }
    },
    methods: {
        getImagePath: function (img) {
            return new URL(`../assets/${img}`, import.meta.url).href;
        }
    }
}
</script>

<template>
    <footer>
        <div>
            <div id="btnContainer">
                <div>
                    <strong>SIGN-UP NOW!</strong>
                </div>
            </div>
            <div id="socialContainer">
                <div>
                    <strong>FOLLOW US</strong>
                </div>
                <img v-for="singleSocialLogo in socialLogo" :src="getImagePath(singleSocialLogo.srcSocialLogo)"
                    :alt="singleSocialLogo.nameSocialLogo">
            </div>
        </div>
    </footer>
</template>

<style scoped>
footer {
    height: 100px;
    background-color: rgba(48, 48, 48, 255);
    display: flex;
    justify-content: center;
}

footer>div {
    height: 100%;
    width: 70%;
    display: flex;
    justify-content: space-between;
}

#btnContainer {
    height: 100%;
    display: flex;
    align-items: center;
}

#btnContainer>div {
    border: 2px solid rgba(2, 130, 249, 255);
    padding: 0.5rem;
}

#btnContainer>div>strong {
    color: white;
}

#socialContainer {
    height: 100%;
    display: flex;
    align-items: center;
}

#socialContainer>div>strong {
    color: rgba(2, 130, 249, 255);
}

#socialContainer>img {
    margin-left: 1rem;
    height: 1.5rem;
}

#socialContainer>img:first-of-type {
    margin-left: 1.5rem;
}
</style>