<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';

// importiamo l'axios
import axios from 'axios';

// importiamo lo store
import { store } from './store';

export default {
  components: {
    AppHeader,
    AppMain
  },

  data() {
    return {
      store
    }
  },

  methods: {
    getCardsYuGiOh() {
      axios
        .get(store.apiInd)
        .then((res) => {
          store.cardsYuArr = res.data.data; // Assegna direttamente i dati ricevuti
          store.loading = false;
          console.log(store.cardsYuArr);
        })
        .catch((err) => {
          console.error("Errore:", err);
        });

    }
  },

  created() {
    this.getCardsYuGiOh();
  }

}
</script>

<template>
  <AppHeader />
  <AppMain />
</template>

<style>
body {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>
