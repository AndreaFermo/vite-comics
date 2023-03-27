<script setup>
import TheHeader from './components/TheHeader.vue'
import TheFooter from './components/TheFooter.vue'
</script>

<template>
  <header>
    <div class="container">
      <TheHeader>
      </TheHeader>
    </div>

  </header>
  <main>
    <div class="container">
      <h1>Content goes here</h1>
    </div>
  </main>
  <footer>
    <div>
      <TheFooter>
      </TheFooter>
    </div>

  </footer>
</template>
<style lang="scss">
@use "./styles/general.scss";
@use "./styles/partials/mixins";

header {
  height: 100px;
}

main {
  height: 300px;
}

footer {
  background-image: url(../src/assets/footer-bg.jpg);
  background-repeat: no-repeat;
  background-size: cover;
}

.container {
  @include mixins.container;
}</style>

