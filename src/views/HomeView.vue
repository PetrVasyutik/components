<template>
  <div class="home">
    <div class="home__container">
      <section class="section">
        <h2>Loader</h2>
        <my-loader />
      </section>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import MyLoader from "@/components/MyLoader.vue";

export default {
  name: "HomeView",
  components: {
    MyLoader,
  },
};
</script>

<style scoped lang="scss">
.home {
  max-width: 1900px;
  margin: 0 auto;
  padding: 30px;

  &__section {
    margin-top: 30px;
    width: 100%;
  }
}
</style>
