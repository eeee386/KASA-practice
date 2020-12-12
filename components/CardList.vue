<template>
  <div>
    <div v-for="card in cards">
      <Card v-bind:card="card"/>
    </div>
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