<script>
import LiveTag from "@/components/LiveTag.vue";

export default {
  components: {
    LiveTag,
  },
  props: {
    tagList: {
      type: Array,
      required: true,
    },
    listLeft: {
      default: false,
      type: Boolean,
    },
  },
};
</script>

<template>
  <div class="list" :class="listLeft && 'list-left'">
    <div
      class="list__item"
      :class="listLeft && 'list-left__item'"
      v-for="(item, index) in tagList"
      :key="item.title"
    >
      <div
        class="list__separator"
        :class="listLeft && 'list-left__separator'"
        v-if="index !== 0"
      >
        <v-icon style="font-size: 6px; vertical-align: middle" color="black"
          >mdi-brightness-1</v-icon
        >
      </div>
      <LiveTag :title="item.title" :icon="item.icon" />
    </div>
  </div>
</template>

<style lang="scss" scoped>
.list {
  // width: 70%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  overflow: hidden;
  flex-wrap: wrap;
  max-height: 22px;
  gap: 8px;

  &__item {
    flex: 1;
    display: inline-flex;
    align-items: center;
    // justify-content: space-around;
    gap: 8px;

    &:nth-child(1) {
      flex: none;
    }
  }

  &__separator {
    margin-left: auto;
    margin-right: auto;
  }

  &-left {
    justify-content: flex-start;

    &__item {
      flex: none;
      justify-content: flex-start;
    }

    &__separator {
      margin: 0;
    }
  }
}
</style>
