<script >
export default {
    name: 'PokemonCard',
    props: {
        name: String,
        type: String,
        serial: String,
        image: String
    }
}
</script>

<template>
    <div class="character-card">
        <img :src="image" :alt="name" class="img-fluid">
        <h3>{{ name }}</h3>
        <div>{{ type }}</div>
        <div>{{ serial }}</div>

    </div>
</template>

<style></style>