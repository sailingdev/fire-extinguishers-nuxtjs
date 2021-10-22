<template>
  <div class="item-container">
    <img
      :src="require(`@/assets/images/${item.image}`)"
      alt=""
    >

    <div class="text-container">
      <h4>{{ item.title }}</h4>
      <p>{{ item.description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    item: {
      type: Object,
      default: null
    }
  }
}
</script>

<style lang="scss" scoped>
.item-container {
  display: flex;
  margin: 3rem 0;

  img {
    width: 17.5rem;
    border-radius: .5rem;
    height: 11rem;
  }

  .text-container {
    padding: 0 1rem;

    p {
      font-size: .8rem;
      color: grey;
    }
  }
;
}
</style>
