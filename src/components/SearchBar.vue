<template>
    <div>
      <input id="search" />
      <button v-on:click="onInput">Greet</button>
    </div>
</template>

<script>
export default {
    name: 'SearchBar',
    methods: {
        onInput: function() {
            console.log(document.getElementById('search').value);
            this.$emit('termChange', document.getElementById('search').value);
        }
    }
};
</script>

<style scoped>
    input {
        width: 75%;
    }

    div {
        text-align:center;
        margin: 20px;
    }
</style>