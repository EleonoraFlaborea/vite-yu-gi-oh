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
    <div class="character-card border border-success rounded border-5">
        <div>
            <img :src="image" :alt="name" class="img-fluid">
        </div>
        <div>
            <h3>{{ name }}</h3>
            <div>Type: {{ type }}</div>
            <div>Serial number: {{ serial }}</div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.character-card {
    background-color: white;
    height: 350px;
    width: 300px;

    display: flex;
    align-items: center;
    flex-wrap: wrap;
    justify-content: center;



    img {
        width: 180px;

    }





}
</style>