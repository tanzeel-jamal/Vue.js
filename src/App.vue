<!-- <script setup></script> -->
<!-- setup is use for composition API-->

<script>
import Counter from "@/components/Counter.vue";
import Header from "@/components/Header.vue";
import Footer from "@/components/Footer.vue";

// Exporting the component using the Options API
export default {
  components: {
    Counter,
    Header,
    Footer,
  },
};
</script>
<template>
  <Header />
  <Counter />
  <Footer />
</template>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>
