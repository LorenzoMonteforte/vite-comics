<script>
import CardContainer from "../components/CardContainer.vue";
export default {
    name: "Jumbotrone",
    components: {
        CardContainer
    },
    data() {
        return {
            cards: [
                {
                    thumb: "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                    price: "$19.99",
                    series: "Action Comics",
                    type: "comic book",
                },
                {
                    thumb: "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                    price: "$3.99",
                    series: "American Vampire 1976",
                    type: "comic book",
                },
                {
                    thumb: "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                    price: "$16.99",
                    series: "Aquaman",
                    type: "graphic novel",
                },
                {
                    thumb: "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                    price: "$2.99",
                    series: "Batgirl",
                    type: "comic book",
                },
                {
                    thumb: "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                    price: "$3.99",
                    series: "Batman",
                    type: "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                    price: "$2.99",
                    series: "Batman Beyond",
                    type: "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                    price: "$3.99",
                    series: "Batman/Superman",
                    type: "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                    price: "$4.99",
                    series: "Batman/Superman Annual",
                    type: "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                    price: "$5.99",
                    series: "Batman: The Joker War Zone",
                    type: "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                    price: "$6.99",
                    series: "Batman: Three Jokers",
                    type: "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                    price: "$4.99",
                    series: "Batman: White Knight Presents: Harley Quinn",
                    type: "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                    price: "$16.99",
                    series: "Catwoman",
                    type: "graphic novel",
                }
            ]
        }
    },
    methods: {
        myToUpperCase: function () {
            for (let i = 0; i < this.cards.length; i++) {
                this.cards[i].series = this.cards[i].series.toUpperCase();
            }
        }
    },
    mounted() {
        this.myToUpperCase();
    }
}
</script>

<template>
    <section>
        <div id="imageContainer"></div>
        <div>
            <div id="centralContainer">
                <div>
                    <div id="currentSeries">
                        <strong>CURRENT SERIES</strong>
                    </div>
                    <CardContainer v-for="card in cards" :srcCard="card.thumb" :titleCard="card.series" />
                </div>
                <div>
                    <div id="loadMore">
                        <strong>LOAD MORE</strong>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped>
#imageContainer {
    height: 300px;
    background-image: url("../assets/img/jumbotron.jpg");
    background-size: cover;
}

section>div:last-child {
    background-color: rgba(12, 9, 18, 255);
    display: flex;
    justify-content: center;
}

#centralContainer {
    width: 70%;
}

#centralContainer>div:first-child {
    position: relative;
    padding: 2rem 0;
    display: flex;
    flex-wrap: wrap;
}

#currentSeries {
    background-color: rgba(2, 130, 249, 255);
    display: inline-block;
    padding: 0.5rem 1rem;
    position: absolute;
    top: 0;
    left: 0;
    translate: 0 -50%;
    color: white;
}

#centralContainer>div:last-child {
    padding-bottom: 1rem;
    display: flex;
    justify-content: center;
    font-size: 0.6rem;
}

#loadMore {
    background-color: rgba(2, 130, 249, 255);
    padding: 0.5rem 2rem;
    color: white;
}
</style>