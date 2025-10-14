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
      <section class="home__section">
        <h2>Glassmorphism</h2>
        <a
          href="https://markodenic.com/tools/glassmorphism-css-generator/"
          target="_blank"
        >
          https://markodenic.com/tools/glassmorphism-css-generator/
        </a>
        <br />
        <br />
        <glass-morphism />
      </section>
      <section class="home__section">
        <h2>OffsetPath</h2>
        <offset-path />
      </section>
      <section class="home__section">
        <h2>Endles scrolling (бесконечная прокрутка)</h2>
        <endless-scrolling />
      </section>
    </div>
    <div class="home__footer"></div>
  </div>
</template>

<script>
// @ is an alias to /src
import MyLoader from "@/components/MyLoader.vue";
import ButtonWithTimer from "@/components/ButtonWithTimer.vue";
import PhotoShutterEffect from "@/components/PhotoShutterEffect.vue";
import GlassMorphism from "@/components/GlassMorphism.vue";
import OffsetPath from "@/components/OffsetPath.vue";
import EndlessScrolling from "@/components/EndlessScrolling.vue";

export default {
  name: "HomeView",
  components: {
    MyLoader,
    ButtonWithTimer,
    PhotoShutterEffect,
    GlassMorphism,
    OffsetPath,
    EndlessScrolling,
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

  &__footer {
    height: 400px;
  }
}
</style>
