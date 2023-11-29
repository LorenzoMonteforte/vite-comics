<script>
export default {
    name: "Jumbotrone"
}
</script>

<template>
    <section>
        <div>
            Content goes here
        </div>
    </section>
</template>

<style scoped>
section {
    height: 100px;
    background-color: black;
    display: flex;
    justify-content: center;
}

section>div {
    height: 100%;
    width: 70%;
    display: flex;
    align-items: center;
    color: white;
}
</style>