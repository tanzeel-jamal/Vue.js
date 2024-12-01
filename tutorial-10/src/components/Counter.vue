<script>
export default {
  data() {
    return {
      counter: 0,
    };
  },
  beforeCreate() {
    console.log("Before creating the component");
  },
  created() {
    console.log("Component created");
  },
  beforeMount() {
    console.log("Before mounting the component");
  },
  mounted() {
    console.log("Component mounted");
  },
  beforeUpdate() {
    console.log("Before updating the component");
  },
  updated() {
    console.log("Component updated");
  },
  beforeUnmount() {
    console.log("Before unmounting the component");
  },
  unmounted() {
    console.log("Component unmounted");
  },
};
</script>

<template>
  <h1>Tanzeel {{ counter }}</h1>
  <br />
  <button @click="counter++">increment</button>
</template>
