<template>
  <div class="center-right-card">
    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
  </div>
</template>

<script>

export default {
  name: 'center-right-card',
}
</script>

<style lang="scss" scoped>
@import './../scss/index.scss';

.center-right-card {
  margin-bottom: 20px;
  padding: 20px;
  display: flex;
  margin-left: 10px;
  flex-direction: flex;
  background: $background-secondary;
  position: relative;
  border-radius: 10px;
  //border: solid;
  box-shadow: 0 2px 5px 5px rgba(0, 0, 0, 0.3);
  //width: calc(49% - ((32px * 2)));


    button {
      margin-top: 5px;
      background: $secondary;
      color: $background-secondary;
      padding: 6px 16px;
      border-radius: 6px;
      box-shadow: 0 10px 27px -11px rgba(0, 0, 0, 0.3);

      &:disabled {
        cursor: not-allowed;
      }
  }
}
</style>
