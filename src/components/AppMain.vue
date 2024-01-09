<script>
import yugiohCard from './yugiohCard.vue';

import { store } from '../store';

export default {
    name: "AppMain",
    components: { yugiohCard },
    data() {
        return {
            store
        }
    }
}

</script>

<template>
    <main>
        <div class="cards" v-for="item in store.cardsYuArr" :key="item">
            <yugiohCard :descrizione="item" />
        </div>
    </main>
</template>

<style lang="scss" scoped>
main {
    width: calc(100vw - 17px);
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;

    .cards {
        width: 20%;
    }

}
</style>