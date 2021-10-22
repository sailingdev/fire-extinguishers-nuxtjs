<template>
  <div class="review-card">
    <div class="image-container">
      <img :src="review.picture.large" alt="">
    </div>
    <div class="text-container">
      <h6>{{ review.login.username }}</h6>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aperiam deleniti eaque enim eum explicabo id incidunt, inventore ipsum magnam natus nihil odit omnis quia quos rerum suscipit vel voluptatem voluptatum.</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    review: {
      type: Object,
      default: null
    }
  }
}
</script>

<style lang="scss" scoped>
.review-card {
  margin-top: 1.5rem;
  height: 4rem;
  display: flex;

  img {
    width: 4rem;
    height: 4rem;
    border-radius: 100%;
  }

  .text-container {
    margin-left: 2rem;

    p {
      color: grey;
    }
  }
}
</style>
