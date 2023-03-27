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
    <div class="container">
      <TheFooter>
      </TheFooter>
    </div>

  </footer>
</template>

<style lang="scss">
@use "./styles/general.scss";
</style>

