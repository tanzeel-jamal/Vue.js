<script>
export default {
  data() {
    return {};
  },
  emits: ["onClick"],
  props: {},
};
</script>

<template>
  <button @click="$emit('onClick', 'Tanzeel is my name')">
    <!-- <slot type="submit">Tanzeel</slot> -->
    <div style="border: 5px solid red" v-if="$slots['left']">
      <slot name="left"></slot>
    </div>
    <slot name="center">CENTER</slot>
    <slot name="right">RIGHT</slot>
  </button>
</template>

<style scoped>
/* .left {
  border: 1px solid black;
} */
</style>
