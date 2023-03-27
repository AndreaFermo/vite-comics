<script setup>
import TheHeader from './components/TheHeader.vue'
import TheFooter from './components/TheFooter.vue'
</script>

<template>
  <header>
    <TheHeader>
    </TheHeader>
  </header>
  <main>
    <h1 class="main-content">Content goes here</h1>
  </main>
  <footer>
    <TheFooter>
    </TheFooter>
  </footer>
</template>

<style>
main {
  color: white;
  background-color: black;

}

.main-content {
  width: 1100px;
  margin: auto;
  line-height: 120px;
}
</style>
