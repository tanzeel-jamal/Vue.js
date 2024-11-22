<template>
  <!-- <Counter /> -->
  <!-- <Accordion :class="{ tanzeel: isActive, unknown: !isActive }" /> -->

  <!-- <Accordion :class="{ isActive ? 'tanzeel':'unknown' }" /> -->
  <Accordion :class="isActive ? 'tanzeel' : 'unknown'" />
  <button @click="toggleActive">Toggle Active</button>

  <!-- <h1 :style="{ color: activeColor, fontSize: fontSize }">adfa</h1> -->
  <h1 :style="styleObject">adfa</h1>

  <h2>{{ obj.nested }}</h2>
  <h2>{{ obj.arr }}</h2>
  <button @click="mutateDeeply">Click</button>
</template>

<script>
// import Counter from "./components/Counter.vue";
// import Accordion from "./components/Accordion.vue";
// export default {
//   components: {
//     // Counter,
//     Accordion,
//   },
//   data() {
//     return {
//       isActive: true, //state
//       //   fontSize: "30px",
//       //   activeColor: "green", //style
//       styleObject: {
//         color: "red",
//         fontSize: "30px",
//       },
//     };
//   },
//   methods: {
//     toggleActive() {
//       this.isActive = !this.isActive; // toggle state
//     },
//   },
// };

export default {
  data() {
    return {
      obj: {
        nested: { count: 0 },
        arr: ["foo", "bar"],
      },
    };
  },
  methods: {
    mutateDeeply() {
      // these will work as expected.
      this.obj.nested.count++;
      this.obj.arr.push("baz");
    },
  },
};
</script>
<!-- <style scoped>
.tanzeel {
  background-color: tan;
}
.unknown {
  background-color: lightgray;
}
</style> -->
