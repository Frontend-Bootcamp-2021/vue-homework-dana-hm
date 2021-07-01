<template>
  <div class="about">
    <h2 class="page-header">About</h2>
    <p class="about__content">
      <img
        src="https://images.unsplash.com/photo-1583512603805-3cc6b41f3edb?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80"
        alt="About Us"
      />
To find the perfect dog for you, you’ll have to do some research. By exploring various breeds, their energy levels, grooming needs and more, you can ensure the dog you bring into your home fits seamlessly into your life. You can use our breed selector, which asks a series of questions about your lifestyle and preferences to suggest appropriate breeds. You can also explore different breeds on our site, sorting by athleticism, appearance and other factors to find the right dog for you.  
    </p>
  </div>
</template>

<script>
import { onMounted, onUnmounted } from "vue";

export default {
  setup() {
    onMounted(() => console.log("Mount: 👓 About Component"));
    onUnmounted(() => console.log("unMount: 👋🏻 About Component "));

    return {};
  },
};
</script>

<style lang="scss">
.about {
  &__content {
    margin: 20px 0;
    padding: 0;

    font-size: 18px;
    line-height: 32px;

    img {
      float: left;

      margin: 0 20px 20px;
    }
  }
}
</style>
