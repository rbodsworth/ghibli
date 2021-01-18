<template lang="html">
    <div class="films-list">
        <ul>
            <list-item v-for="(film, index) in films" v-bind:film="film" v-bind:key="index"></list-item>
        </ul>
    </div>
</template>

<script>
    import ListItem from './ListItem.vue';
    export default {
        name: 'films-list',
        props: ['films'],
        components: {
            "list-item": ListItem
        }
    }
</script>

<style lang="css" scoped>

.films-list {
  width: 1000%;
  height: 550px;
  overflow-y: scroll;
  display: flex;
  flex-wrap: wrap;
  font: futura;
  pointer-events: fill;
  
}
</style>