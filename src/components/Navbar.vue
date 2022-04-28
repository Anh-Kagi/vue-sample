<script lang="ts" setup>
import Logo from "./Logo.vue";
</script>

<script lang="ts">
export default {
  data: () => ({
    isMenuActive: false,
  }),
};
</script>

<template>
  <nav class="navbar is-primary">
    <div class="navbar-brand mx-2">
      <a href="/" class="is-flex is-align-items-center">
        <Logo />

        <span class="navbar-item is-size-3">A Définir</span>
      </a>

      <a
        role="button"
        class="navbar-burger"
        :class="{ 'is-active': isMenuActive }"
        aria-label="menu"
        aria-expanded="false"
        data-target="navbarBasicExample"
        @click="isMenuActive = !isMenuActive"
      >
        <span aria-hidden="true"></span> <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
      </a>
    </div>

    <div class="navbar-menu pl-5" :class="{ 'is-active': isMenuActive }">
      <div class="navbar-start">
        <a class="navbar-item"> Home </a>

        <a class="navbar-item"> Documentation </a>

        <div class="navbar-item has-dropdown is-hoverable">
          <a class="navbar-link"> More </a>

          <div class="navbar-dropdown">
            <a class="navbar-item"> About </a>
            <a class="navbar-item"> Jobs </a>
            <a class="navbar-item"> Contact </a>
            <hr class="navbar-divider" />
            <a class="navbar-item"> Report an issue </a>
          </div>
        </div>
      </div>

      <div class="navbar-end">
        <div class="navbar-item">
          <div class="buttons">
            <a class="button is-primary">
              <strong>Sign up</strong>
            </a>
            <a class="button is-light"> Log in </a>
          </div>
        </div>
      </div>
    </div>
  </nav>
</template>

<style lang="scss" scoped>
@import "@/style/settings.scss";

.navbar-brand {
  align-items: center;
}
</style>
