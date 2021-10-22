<!-- eslint-disable vue/attribute-hyphenation -->
<template>
  <div>
    <div class="container">
      <Hero />

      <CardsDisplay
        v-for="cardInfo in largeCardSections"
        :key="cardInfo.id"
        :cardSection="cardInfo"
      />

      <SmallCardsDisplay
        v-for="cardInfo in smallCardSections"
        :key="cardInfo.id"
        :cardSection="cardInfo"
      />
    </div>
  </div>
</template>

<script>
import { largeCardSections, smallCardSections } from '@/assets/data'

export default {
  data () {
    return {
      largeCardSections, smallCardSections
    }
  }
}
</script>

<style lang="scss" scoped>

</style>
