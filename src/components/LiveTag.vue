<script>
export default {
  props: {
    title: {
      type: String,
      required: true,
    },
    icon: String,
  },
};
</script>

<template>
  <div class="live-tag">
    <v-icon v-if="!!icon">{{ icon }}</v-icon>
    <span class="live-tag__name">
      {{ title }}
    </span>
  </div>
</template>

<style lang="scss" scoped>
.live-tag {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 5px;

  &__name {
    color: rgba(0, 0, 0, 0.54);
    white-space: nowrap;
  }
}
</style>
