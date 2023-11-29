<script>
import Jumbotrone from "./Jumbotrone.vue";
import SecondSection from "./SecondSection.vue";
import ThirdComponent from "./ThirdComponent.vue";
export default {
    name: "MainComponent",
    components: {
        Jumbotrone,
        SecondSection,
        ThirdComponent
    }
}
</script>

<template>
    <main>
        <Jumbotrone />
        <SecondSection />
        <ThirdComponent />
    </main>
</template>

<style scoped></style>