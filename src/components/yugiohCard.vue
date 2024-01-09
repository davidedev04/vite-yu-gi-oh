<script>

export default {
    name: "yugiohCard",
    props: {
        descrizione: Object
    }
}

</script>

<template>
        <div class="card">
            <img :src="descrizione.card_images[0].image_url" alt="">
            <h3>{{ descrizione.name }}</h3>
            <span>{{ descrizione.archetype }}</span>
        </div>
</template>

<style scoped>
.card {
    height: 350px;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    background-color: #d48f38;
    margin: 5px;

    img {
        height: 250px;
        width: 200px;
    }
}
</style>