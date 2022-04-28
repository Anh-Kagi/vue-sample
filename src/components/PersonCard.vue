<script lang="ts" setup></script>

<script lang="ts">
export default {
  props: { title: String, icon: String, img: String, role: String },
};
</script>

<template>
  <div
    class="tile is-vertical card m-3"
    v-if="
      img != undefined ||
      title != undefined ||
      icon != undefined ||
      role != undefined
    "
  >
    <div class="card-image" v-if="img != undefined">
      <figure class="image is-1by1">
        <img :src="img" alt="Card Image" />
      </figure>
    </div>
    <div class="card-header" v-if="title != undefined || icon != undefined">
      <div class="card-header-icon" v-if="icon != undefined">
        <figure class="image">
          <img id="icon" :src="icon" alt="Person Icon" />
        </figure>
      </div>
      <div class="card-header-title" v-if="title != undefined">
        {{ title }}
      </div>
    </div>
    <div class="card-content" v-if="role != undefined">
      {{ role }}
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import "@/style/settings.scss";

#icon {
  height: 3em;
  transition: transform 0.2s $easing;
}

#icon:hover {
  transform: scale(1.2);
}
</style>
