<template>
  <div class="container">
    <h3 class="header">
      {{ cardSection.title }}
    </h3>
    <div class="cards-container">
      <SmallCard
        v-for="card in cardSection.cards"
        :key="card.id"
        :card="card"
      />
    </div>
  </div>
</template>

<script>
export default {
  props: {
    cardSection: {
      type: Object,
      default: null
    }
  }
}
</script>

<style lang="scss" scoped>
.container {
  padding: 2rem 0;

  .header {
    font-weight: 700;
    font-size: 1.5rem;
    margin-bottom: 2rem;
  }

  .cards-container {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
  }
}
</style>
