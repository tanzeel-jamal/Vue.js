<script>
import Counter from "./components/Counter.vue";

export default {
  data() {
    return {
      show: false,
    };
  },
  components: {
    Counter,
  },
};
</script>

<template>
  <Counter v-if="show" />
  <button @click="show = !show">Toggle</button>
</template>
