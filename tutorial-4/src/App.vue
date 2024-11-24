<template>
  <!-- <h1>{{ data }}</h1>
  <h1>{{ data.length }}</h1>

  <h2>{{ isEvenOrOdd() }}</h2>
  <h2>{{ isEvenOrOdd() }}</h2>
  <h2>{{ isEvenOrOdd() }}</h2>

  <h1>{{ evenOrOdd }}</h1>
  <h1>{{ evenOrOdd }}</h1>
  <h1>{{ evenOrOdd }}</h1>

  <button @click="addinfo">Add Info</button>
  <button @click="counter++">Increment {{ counter }}</button> -->
  <div :class="classObject">Tanzeel</div>
</template>

<script>
// export default {
//   data() {
//     return {
//       counter: 1,
//       data: [
//         { id: 1, name: "John", age: 25 },
//         { id: 2, name: "Jane", age: 30 },
//         { id: 3, name: "Alice", age: 28 },
//         { id: 4, name: "Bob", age: 32 },
//       ],
//     };
//   },
//   computed: {
//     evenOrOdd() {
//       console.log("computed called");
//       return this.data.length % 2 === 0 ? "even" : "odd";
//     },
//   },
//   methods: {
//     isEvenOrOdd() {
//       console.log("method called");
//       return this.data.length % 2 === 0 ? "even" : "odd";
//     },
//     addinfo() {
//       this.data.push({ id: 5, name: "Charlie", age: 35 });
//     },
//   },
// };

export default {
  data() {
    return {
      isActive: true,
      // error: {
      //   type: "fatal",
      // },
      error: null,
    };
  },
  computed: {
    classObject() {
      return {
        active: this.isActive && !this.error,
        "text-danger": this.error && this.error.type === "fatal",
      };
    },
  },
};
</script>

<style scoped>
.active {
  background-color: green;
}
.text-danger {
  color: red;
}
</style>
