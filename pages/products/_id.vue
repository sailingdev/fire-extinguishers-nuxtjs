<template>
  <div>
    <div v-if="product" class="container py-5">
      <div class="hero-container">
        <img
          :src="require(`@/assets/images/${product.image}`)"
          alt=""
          class="image"
        >
        <div class="info-box">
          <h1>{{ product.title }}</h1>
          <p class="snippet">
            {{ product.snippet }}
          </p>
          <RentModal :product="product" />
        </div>
      </div>

      <div class="whats-included-container">
        <div class="included-container">
          <h6>Supper Effective</h6>
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam aspernatur dolore dolorum earum exercitationem illo illum inventore ipsa iure, neque nisi nostrum perferendis qui quis quos repellat velit vero voluptatibus!</p>
        </div>
        <div class="included-container">
          <h6>Clean & Tidy</h6>
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam aspernatur dolore dolorum earum exercitationem illo illum inventore ipsa iure, neque nisi nostrum perferendis qui quis quos repellat velit vero voluptatibus!</p>
        </div>
        <div class="included-container">
          <h6>Cancel Anytime</h6>
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam aspernatur dolore dolorum earum exercitationem illo illum inventore ipsa iure, neque nisi nostrum perferendis qui quis quos repellat velit vero voluptatibus!</p>
        </div>
        <div class="included-container">
          <h6>Satisfaction Guaranteed</h6>
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam aspernatur dolore dolorum earum exercitationem illo illum inventore ipsa iure, neque nisi nostrum perferendis qui quis quos repellat velit vero voluptatibus!</p>
        </div>
      </div>

      <div class="description-container">
        <p>
          {{ product.description }}
        </p>
      </div>

      <Reviews />
    </div>

    <div v-else class="container padding">
      <PageNotFound />
    </div>
  </div>
</template>

<script>
export default {
  computed: {
    product () {
      return this.$store.getters.getProductById(this.$route.params.id)
    }
  }
}
</script>

<style lang="scss" scoped>
.hero-container {
  display: flex;
  justify-content: space-between;

  .image {
    width: 59%;
    height: 25rem;
  }

  .info-box {
    width: 39%;
    background-color: rgba(207, 201, 201, .322);
    padding: 1rem;
    border-radius: .5rem;

    .snippet {
      color: rgba(0, 0, 0, .774);
      margin-top: 1rem;
    }
  }
}

.whats-included-container {
  border-bottom: .1rem solid rgba(128, 128, 128, .151);

  .included-container {
    margin-top: 1.5rem;
  }
}

.description-container {
  border-bottom: .1rem solid rgba(128, 128, 128, .151);
  padding-bottom: 2rem;
  margin-bottom: 2rem;
  margin-top: 3rem;
  color: grey;
}

h1 {
  font-size: 1.75rem;
}
h6 {
  font-size: 1.15rem;
  font-weight: 400;
}
p {
  color: grey
}

div.padding {
  padding: 10rem 0;
}
</style>
