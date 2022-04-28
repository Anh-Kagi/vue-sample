<script lang="ts" setup>
import Navbar from "./components/Navbar.vue";
import Hero from "./components/Hero.vue";
import PersonCard from "./components/PersonCard.vue";
import Footer from "./components/Footer.vue";
</script>

<script lang="ts">
export default {};
</script>

<template>
  <header>
    <Navbar />
  </header>

  <main>
    <Hero />

    <!-- presentation -->
    <section class="section has-background-dark">
      <div class="title has-text-centered">Team</div>
      <div class="tile is-ancestor">
        <PersonCard
          title="J. Doe"
          icon="/logo.svg"
          img="/logo-outlined.svg"
          role="CEO"
        />
        <PersonCard
          title="A. Smith"
          icon="/logo.svg"
          img="/logo-outlined.svg"
          role="Product Designer"
        />
        <PersonCard
          title="A. Smithee"
          icon="/logo.svg"
          img="/logo-outlined.svg"
          role="Head of development"
        />
        <PersonCard
          title="B. Wayne"
          icon="/logo.svg"
          img="/logo-outlined.svg"
          role="Head of marketing"
        />
      </div>
    </section>
  </main>

  <Footer />
</template>

<style lang="scss">
@import "@/style/base.scss";
</style>
