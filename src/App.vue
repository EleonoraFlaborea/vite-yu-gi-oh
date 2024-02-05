<script>
import axios from 'axios';
import { store } from './data/store.js'
const endpoint = 'https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons'

import AppMain from './components/AppMain.vue';
export default {
  name: 'MyApp',
  components: { AppMain },

  created() {
    axios.get(endpoint).then(res => {
      store.characters = res.data.results;
    })
  }
}
</script>

<template>
  <AppMain />
</template>

<style lang="scss" scoped>
@use './assets/scss/style.scss';
</style>
