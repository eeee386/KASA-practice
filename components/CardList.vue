<template>
  <div class="card-list">
    <Card v-for="card in cards" v-bind:card="card"/>
  </div>
</template>

<script>
import Card from './Card';

export default {
  name: "CardList",
  components: {
    Card
  },
  props: ["cards"]
}
</script>

<style scoped>
.card-list {
  display: flex;
  justify-content: space-around;
}
</style>