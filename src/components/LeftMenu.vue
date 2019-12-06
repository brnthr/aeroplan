<template>
    <div class="left-menu">
        <span class="title">Menu</span>
        <div class="buttons">
      <router-link tag="button" :to="{ name: 'avion' }">
        Avion
      </router-link>

      <router-link tag="button" :to="{ name: 'reterd' }">
        Retard
      </router-link>

      <router-link tag="button" :to="{ name: 'mouvement' }">
        Mouvement
      </router-link>

      <router-link tag="button" :to="{ name: 'aéroport' }">
        Aéroport
      </router-link>
    </div>
    </div>
</template>

<style lang="scss" scoped>
@import './src/scss/index.scss';

.left-menu {
  display: flex;
  justify-content: flex-start;
  flex-direction: column;
  height: 100vh;
  //border: solid;
  //border-radius: 10px;
  box-shadow: 0 2px 5px 5px rgba(0, 0, 0, 0.3);
  background: $background-primary;

  .title {
    font-weight: bold;
    padding: 16px;
  }

  .buttons {
    display: flex;
    flex-direction: column;
    margin-left: 5px;

    button {
      display: flex;
      flex-direction: row;
      align-items: center;
      padding: 8px 16px;
      margin: 4px 0;
      width: 100%;
      border-radius: 5px;

      // Transition du background
      background-color: $background-secondary;
      background-image: linear-gradient(-90deg, white, rgba(255,255,255,0));
      transition: background .2s ease-in-out;

      &:hover {
        background-color: $secondary-light;
      }

      &.router-link-exact-active {
        background-color: $secondary-light;
        color: $secondary;
      }
    }
  }

  .title-container {
    display: flex;
    justify-content: flex-start;
    align-items: center;

    .title {
      padding-right: 8px;
    }

    .type-quantity {
      font-size: 12px;
    }
  }

  .types-buttons {
    flex-grow: 1;
    display: flex;
    flex-direction: column;
    overflow-y: scroll;
    padding: 0 24px;
    margin-bottom: 32px;

    button.type {
      padding: 7px 0;
      display: flex;
      justify-content: space-between;
      align-items: center;

      &:hover {
        span.type-name {
          text-decoration: underline;
        }
      }

      span.book-quantity {
        font-size: 12px;
        font-weight: 400;
      }
    }
  }

  .lib-title-container {
    display: flex;

    .title {
      flex-grow: 1;
    }

    .change {
      font-size: 14px;
      padding-right: 16px;
      text-decoration: underline;
      cursor: pointer;
    }
  }
}
</style>
