<template>
  <div class="content">
    <HeaderCard />
    <Card />
    <div class="content-card">
    <CenterLeftCard />
    <CenterRightCard />
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import HeaderCard from '@/components/HeaderCard.vue';
import Card from '@/components/Card.vue';
import CenterLeftCard from '@/components/CenterLeftCard.vue';
import CenterRightCard from '@/components/CenterRightCard.vue';

export default {
  name: 'content',
  components: {
    HeaderCard,
    Card,
    CenterLeftCard,
    CenterRightCard
  }
}
</script>

<style lang="scss" scoped>
@import './src/scss/index.scss';

.content {
  padding: 20px;
  //border: solid;
  border-radius: 10px;
  overflow-x: scroll;

  .content-card {
    display: flex;

  }

  .title {
    font-weight: bold;
    font-size: 16px;
    text-transform: uppercase;
    margin-bottom: 20px;

    }

  .borrow-card {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-top: auto;

    .available {
      color: $secondary;
      margin-bottom: 10px;
      font-weight: 500;

      &.not {
        color: #BF211E;
      }
    }

    .error {
      color: #BF211E;
      font-weight: 500;
      margin-bottom: 10px;
    }

    button {
      background: $secondary;
      color: $background-secondary;
      padding: 6px 16px;
      border-radius: 6px;
      box-shadow: 0 10px 27px -11px rgba(0, 0, 0, 0.3);
      transition: transform ease .2s;

      &:disabled {
        cursor: not-allowed;
        opacity: .75;
        &:hover {
          transform: none;
        }
      }

      &:hover {
        transform: scale(1.1);
      }
    }
  }

}
</style>