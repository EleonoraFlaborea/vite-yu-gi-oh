<script >

import { store } from '../data/store.js';
import PokemonCard from './PokemonCard.vue'
export default {
    name: 'PokemonList',
    data: () => ({ store }),
    components: { PokemonCard },
}
</script>

<template>
    <section>
        <div class="row g-3">
            <div class="col" v-for="character in store.characters" :key="character.id">
                <PokemonCard :name="character.name" :image="character.imageUrl" />
            </div>
        </div>

    </section>
</template>

<style></style>