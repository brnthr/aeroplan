<template>
  <div class="home">
    <LeftMenu />
    <Content />
  </div>
</template>

<script>
// @ is an alias to /src
import LeftMenu from '@/components/LeftMenu.vue';
import Content from '@/components/Content.vue';

export default {
  name: 'home',
  components: {
    LeftMenu,
    Content
  }
}
</script>

<style lang="scss" scoped>
@import './src/scss/index.scss';

.home {
  display: flex;
  flex-direction: row;
  flex-wrap: nowrap;
  align-items: flex-start;
  height: 100%;
  color: $primary;

  .page {
    display: flex;
    flex-grow: 1;
    height: calc(100% - 75px);

    .left-menu {
      background: $background-secondary;
      min-width: 250px;
      max-width: 250px;
    }

    .content {
      flex-grow: 1;
      overflow: scroll;

      & > div {
        display: flex;
        justify-content: flex-start;
        padding: 32px;
      }
    }
  }
}
</style>