<script lang="ts" setup>
import NavBar from "./components/NavBar.vue";
</script>

<script lang="ts">
export default {};
</script>

<template>
  <header>
    <NavBar />
  </header>
  <!-- hero -->
  <!-- presentation -->
  <!-- team -->
  <!-- footer -->
</template>

<style lang="scss">
@import "@/style/base.scss";
</style>

<style lang="scss" scoped>
@import "@/style/settings.scss";
header {
  background-color: $primary;
  border-radius: 0 0 0.5rem 0.5rem;
}
</style>
