<script lang="ts">
export default {};
</script>

<template>
  <img src="/logo-outlined.svg" alt="Logo" />
</template>

<style lang="scss" scoped>
@import "@/style/settings.scss";

img {
  height: 3em;
  transition: transform 0.2s $easing;
}

img:hover {
  transform: scale(1.2);
}
</style>
