<template>
  <div class="home">
    <div class="home__container">
      <section class="home__section">
        <h2>Loader</h2>
        <my-loader />
      </section>
      <section class="home__section">
        <h2>Buttons</h2>
        <div class="home__row">
          <div>
            <h3>Button with timer</h3>
            <button-with-timer />
          </div>
        </div>
      </section>
      <section class="home__section">
        <h2>Photo shutter effect(hover)</h2>
        <photo-shutter-effect />
      </section>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import MyLoader from "@/components/MyLoader.vue";
import ButtonWithTimer from "@/components/ButtonWithTimer.vue";
import PhotoShutterEffect from "@/components/PhotoShutterEffect.vue";

export default {
  name: "HomeView",
  components: {
    MyLoader,
    ButtonWithTimer,
    PhotoShutterEffect,
  },
};
</script>

<style scoped lang="scss">
.home {
  max-width: 1900px;

  h2,
  h3 {
    margin-top: 0;
  }

  &__container {
    margin: 0 auto;
    padding: 30px;
  }

  &__section {
    margin-top: 50px;
    width: 100%;
  }

  &__row {
    display: flex;
    gap: 20px;
  }
}
</style>
