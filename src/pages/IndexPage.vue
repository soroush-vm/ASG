<template>
  <q-page padding>
    <div class="q-intersection-container">
      <default-card v-for="(card, index) in items" v-bind="card" :key="index"> </default-card>
    </div>
  </q-page>
</template>

<script setup>
import DefaultCard from 'src/components/DefaultCard.vue'
import { ref } from 'vue'

const items = ref([
  { id: 1, title: 'Card 1', subtitle: 'Subtitle 1' },
  { id: 2, title: 'Card 2', subtitle: 'Subtitle 2' },
  { id: 3, title: 'Card 3', subtitle: 'Subtitle 3' },
  { id: 4, title: 'Card 4', subtitle: 'Subtitle 4' },
  { id: 5, title: 'Card 5', subtitle: 'Subtitle 5' },
  { id: 6, title: 'Card 6', subtitle: 'Subtitle 6' },
  { id: 7, title: 'Card 7', subtitle: 'Subtitle 7' },
  { id: 8, title: 'Card 8', subtitle: 'Subtitle 8' },
])
</script>
<style lang="scss" scoped>
.q-intersection-container {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
}
@media (max-width: 1830px) {
  .q-intersection-container {
    grid-template-columns: repeat(4, 1fr);
  }
}
@media (max-width: 1530px) {
  .q-intersection-container {
    grid-template-columns: repeat(3, 1fr);
  }
}
@media (max-width: 1200px) {
  .q-intersection-container {
    grid-template-columns: repeat(2, 1fr);
  }
}
@media (max-width: 900px) {
  .q-intersection-container {
    grid-template-columns: repeat(1, 1fr);
  }
}
</style>
