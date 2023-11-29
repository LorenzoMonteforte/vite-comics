<script>
import Jumbotrone from "./Jumbotrone.vue";
import SecondSection from "./SecondSection.vue";
export default {
    name: "MainComponent",
    components: {
        Jumbotrone,
        SecondSection
    }
}
</script>

<template>
    <main>
        <Jumbotrone />
        <SecondSection />
    </main>
</template>

<style scoped></style>