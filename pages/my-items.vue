<template>
  <div class="container">
    <MyItem
      v-for="item in myRentals"
      :key="item.id"
      :item="item"
    />
  </div>
</template>

<script>
import { mapState } from 'vuex'

export default {
  layout: 'no-nav',
  computed: {
    ...mapState([
      'myRentals'
    ])
  }
}
</script>

<style lang="scss" scoped>

</style>
