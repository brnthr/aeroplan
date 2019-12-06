<template>
  <div class="card">
  </div>
</template>

<script>

export default {
  name: 'card',
}
</script>

<style lang="scss" scoped>
@import './src/scss/index.scss';

.card {
  margin-bottom: 20px;
  padding: 20px;
  display: flex;
  flex-direction: flex;
  background: $background-secondary;
  position: relative;
  border-radius: 10px;
  //border: solid;
  box-shadow: 0 2px 5px 5px rgba(0, 0, 0, 0.3);

  .card-info {
    padding-right: px;
    display: flex;
    flex-direction: column;

    .title {
      font-weight: bold;
      margin-bottom: 10px;
    }

    .description {
      font-size: 14px;
      height: 75px;
      margin-top: 6px;
      overflow: hidden;
      position: relative;

      &::before {
        position: absolute;
        content: '';
        background: linear-gradient(transparent 20px, white);
        width: 100%;
        height: 100%;
      }
    }

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
}
</style>
