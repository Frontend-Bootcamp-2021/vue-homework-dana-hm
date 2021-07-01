<template>
  <div class="home">
    <h2 class="page-header">Home</h2>
    <header class="home__header">
      <h3 class="home__title">
Adopting a dog is a big step. There are a lot of things to consider, from choosing the right one for your lifestyle to deciding where to adopt from. Let us help you find the perfect canine companion.        </h3>
    </header>
  </div>
</template>

<script>
import { onMounted, onUnmounted } from "vue";
export default {
  setup() {
    onMounted(() => console.log("Mount: ⛰ Home Component"));
    onUnmounted(() => console.log("unMount: 👋🏻 Home Component "));

    return {};
  },
};
</script>

<style lang="scss">
.home {
  display: flex;
  flex-direction: column;
  align-items: stretch;
  justify-content: flex-start;

  &__header {
    flex-grow: 1;

    margin: 0;
    padding: 20px;

    min-height: 120px;

    display: flex;
    flex-direction: row;
    align-items: flex-start;
    justify-content: flex-start;

    background-color: $blue;
    color: $white;
  }
}
</style>
