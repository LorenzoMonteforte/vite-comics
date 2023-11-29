<script>
export default {
    name: "HeaderComponent",
    data() {
        return {
            links: [
                {
                    nameLink: "CHARACTERS",
                    srcLink: ""
                },
                {
                    nameLink: "COMICS",
                    srcLink: ""
                },
                {
                    nameLink: "MOVIES",
                    srcLink: ""
                },
                {
                    nameLink: "TV",
                    srcLink: ""
                },
                {
                    nameLink: "GAMES",
                    srcLink: ""
                },
                {
                    nameLink: "COLLECTIBLES",
                    srcLink: ""
                },
                {
                    nameLink: "VIDEOS",
                    srcLink: ""
                },
                {
                    nameLink: "FANS",
                    srcLink: ""
                },
                {
                    nameLink: "NEWS",
                    srcLink: ""
                },
                {
                    nameLink: "SHOP",
                    srcLink: ""
                }
            ]
        }
    }
}
</script>

<template>
    <header>
        <div>
            <div id="logoContainer">
                <img src="../assets/img/dc-logo.png" alt="Logo DC">
            </div>
            <nav>
                <ul>
                    <li v-for="link in links">
                        <strong>
                            <a href="">{{ link.nameLink }}</a>
                        </strong>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<style scoped>
header {
    height: 100px;
    display: flex;
    justify-content: center;
}

header>div {
    height: 100%;
    width: 70%;
    display: flex;
    justify-content: space-between;
}

#logoContainer {
    height: 100%;
    padding: 1rem 0;
}

#logoContainer>img {
    height: 100%;
}

nav {
    height: 100%;
}

nav>ul {
    height: 100%;
    display: flex;
    gap: 1.5rem;
}

nav>ul>li {
    display: flex;
    align-items: center;
    border-bottom: 3px solid transparent;
}

nav>ul>li>strong a {
    font-size: 0.6rem;
    color: black;
}

/* Hover */
nav>ul>li:hover a {
    color: rgba(2, 130, 249, 255);
}

nav>ul>li:hover {
    border-bottom: 3px solid rgba(2, 130, 249, 255);
}
</style>