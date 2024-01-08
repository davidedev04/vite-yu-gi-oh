<script>

export default {
    name: "AppHeader"
}

</script>

<template>
    <header>
        <div class="d-logo-span">
            <img src="../assets/Yugioh_anime_logo.webp" alt="logo">
            <span>
                Yu-Gi-Oh Api
            </span>
        </div>
    </header>
</template>

<style lang="scss" scoped>
header {
    width: 100vw;
    height: 80px;
    background-color: #fff;
    display: flex;
    align-items: center;

    .d-logo-span {
        display: flex;
        align-items: center;
        margin-left: 20px;

        img {
            height: 30px;
        }

        span {
            font-size: 30px;
        }

    }



}
</style>