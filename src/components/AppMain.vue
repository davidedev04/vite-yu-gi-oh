<script>
import yugiohCard from './yugiohCard.vue';

import { store } from '../store';

export default {
    name: "AppMain",
    components: { yugiohCard },
    data(){
        return{
            store
        }
    }
}

</script>

<template>
    <main>
        <div class="container" v-for="item in store.cardsYuArr" :key="item">
            <yugiohCard :descrizione="item" />
        </div>
    </main>
</template>

<style lang="scss" scoped>
main {
    width: 100%;
    height: calc(100vh - 80px);
    background-color: #d48f38;

    .container{
        background-color: #fff;
    }

}
</style>