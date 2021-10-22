<template>
  <div class="container">
    <h4 class="header">
      {{ cardSection.title }}
    </h4>
    <p class="snippet">
      {{ cardSection.snippet }}
    </p>
    <div class="cards-container">
      <Card
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
  margin-top: 2rem;

  .header {
    font-weight: 700;
    font-size: 1.5rem;
  }

  .snippet {
    color: grey;
    margin-bottom: 1.5rem;
  }

  .cards-container {
    display: flex;
    justify-content: space-between;
  }
}
</style>
