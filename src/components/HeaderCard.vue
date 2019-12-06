<template>
  <div class="header-card">
    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Nisi scelerisque eu ultrices vitae. Nunc aliquet bibendum enim facilisis gravida neque convallis. Ac felis donec et odio pellentesque diam volutpat. Eu augue ut lectus arcu bibendum at varius. Scelerisque in dictum non consectetur a erat nam at. Adipiscing enim eu turpis egestas pretium aenean pharetra magna. 
  </div>
</template>

<script>

export default {
  name: 'header-card',
}
</script>

<style lang="scss" scoped>
@import './src/scss/index.scss';

.header-card {
  margin-bottom: 20px;
  padding: 20px;
  display: flex;
  flex-direction: flex;
  background: $background-secondary;
  position: relative;
  border-radius: 10px;
  //border: solid;
  box-shadow: 0 2px 5px 5px rgba(0, 0, 0, 0.3);
  //width: calc(49% - ((32px * 2)));

  .header-info {
    padding-right: px;
    display: flex;
    flex-direction: column;

    .title {
      font-weight: bold;
      margin-bottom: 10px;

      .author {
        opacity: (.4);
        font-weight: normal;
      }
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
