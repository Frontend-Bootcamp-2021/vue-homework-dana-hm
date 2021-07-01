<template>
  <div class="content">
    <HeaderComponent />
    <h1> How To Adapt A Dog</h1>
    <router-view />
    <FooterComponent />
  </div>
</template>

<script>
import HeaderComponent from "./components/shared/Header.vue";
import FooterComponent from "./components/shared/Footer.vue";
export default {
  components: { HeaderComponent, FooterComponent },
  setup() {
    return {};
  },
};
</script>

<style lang="scss">
.content {
    display:flex;
    flex-direction: column;
    justify-content: center;
    margin: 0 auto;
}
</style>
