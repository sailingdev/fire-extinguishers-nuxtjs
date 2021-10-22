<!--
eslint-disable vue/attribute-hyphenation
-->
<template>
  <div class="products-container">
    <CardsDisplay
      v-for="cardInfo in largeCardSections.slice(0, 1)"
      :key="cardInfo.id"
      :cardSection="cardInfo"
    />
    <SmallCardsDisplay
      v-for="cardInfo in smallCardSections"
      :key="cardInfo.id"
      :cardSection="cardInfo"
    />
  </div>
</template>

<script>
import { largeCardSections, smallCardSections } from '../../assets/data'

export default {
  data () {
    return {
      largeCardSections, smallCardSections
    }
  }
}
</script>

<style lang="scss" scoped>
.products-container {
  margin: auto;
}
</style>
