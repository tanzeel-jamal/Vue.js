<script>
import Button from "./components/Button.vue";
export default {
  components: { Button },
  data() {
    return {
      buttonText: "Click me",
      show: "left",
    };
  },
  methods: {
    con(value) {
      console.log("Button clicked", value);
    },
    toggle() {
      this.buttonText =
        this.buttonText === "Click me" ? "Changed content" : "Click me";
    },
  },
};
</script>

<template>
  <!-- <Button :text="'Click me'" @on-click="con" /> -->
  <Button @on-click="con">
    <!-- {{ buttonText }} -->
    <template #[show]>rafe </template>

    <template #center> center </template>

    <!-- <template v-slot:right> <h1>Right</h1> </template> -->
  </Button>
  <button @click="toggle">Changed</button>
  <button @click="show = 'right'">Toggle</button>
</template>
