<script>

export default {
    name: "yugiohCard",
    props: {
        descrizione: Object
    }
}

</script>

<template>

    <main>
        <div class="card">
            <img :src="descrizione.card_images[0].image_url" alt="">
            <h5>{{descrizione.name}}</h5>
            <span>{{descrizione.archetype}}</span>
        </div>
    </main>

</template>

<style scoped>

</style>