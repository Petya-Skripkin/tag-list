<script>
import HomeHeader from "@/components/HomeHeader.vue";
import TagList from "@/components/TagList.vue";
import NewFooter from "@/components/NewFooter.vue";

export default {
  name: "App",

  components: {
    HomeHeader,
    TagList,
    NewFooter
  },

  data: () => ({
    tagList: [
      { title: "5", icon: "mdi-star" },
      { title: "Просто чума)", icon: "mdi-emoticon-cool-outline" },
      { title: "Многие люди" },
      { title: "Некоторым персонам", icon: "mdi-contacts-outline" },
      { title: "Звездато!" },
    ],
  }),
};
</script>

<template>
  <v-app>
    <HomeHeader />

    <v-main>
      <div class="content">
        <h2 class="content__title">Понеслась😀</h2>
        <div class="content__item">
          <div class="content__card"><TagList :tagList="tagList" /></div>
          <div class="content__sheet"><TagList :tagList="tagList" /></div>
        </div>
        <h2 class="content__title">Внутренний покой😌</h2>
        <div class="content__item">
          <div class="content__card"><TagList :tagList="tagList" :listLeft="true" /></div>
          <div class="content__sheet">
            <TagList :tagList="tagList" :listLeft="true" />
          </div>
        </div>
        <h2 class="content__title">Что-то очень важное)</h2>
        <div class="content__item">
          <div class="content__card"><TagList :tagList="tagList" :listLeft="true" /></div>
          <div class="content__sheet">
            <TagList :tagList="tagList" />
          </div>
        </div>
        <h2 class="content__title">Уф, надеюсь все😄</h2>
        <div class="content__item">
          <div class="content__card"><TagList :tagList="tagList" /></div>
          <div class="content__sheet">
            <TagList :tagList="tagList" :listLeft="true" />
          </div>
        </div>
      </div>
    </v-main>
    <NewFooter />
  </v-app>
</template>

<style lang="scss">
.content {
  display: flex;
  flex-wrap: wrap;
  gap: 5px;
  padding: 5px 16px;
  margin-top: 20px;

  &__title {
    margin-left: 16px;
  }

  &__item {
    width: 100%;
    display: flex;
    gap: 5px;
  }

  &__card {
    width: 30%;
    padding: 10px 15px;
  }

  &__sheet {
    width: 70%;
    border: 1px solid black;
    padding: 10px 15px;
  }
}
</style>
