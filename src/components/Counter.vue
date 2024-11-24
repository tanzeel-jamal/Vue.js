<template>
  <h1>Counter</h1>
  <div class="counter-wrapper">
    <h2 v-bind:class="counterStyle">
      Count: {{ counter > 10 ? "yes" : "no" }}
      <!-- Count: {{ isDivisibleBy4(counter) }} -->
    </h2>

    <!-- @click is a event which will run on click  -->
    <button @click="incrementCounter">Increment</button>
    <button @click="resetCounter">Reset</button>
    <button @click="decrementCounter">Decrement</button>
  </div>
</template>
<script>
export default {
  data() {
    // data always returns a object
    return {
      counterStyle: "normal", // default style
      counter: 0, // also know as state  which contains some information
    };
  },
  methods: {
    incrementCounter() {
      this.counter++;
      if (this.counter > 0) {
        this.counterStyle = "success";
      }
    },
    decrementCounter() {
      this.counter--;
      if (this.counter < 0) {
        this.counterStyle = "danger";
      }
    },
    resetCounter() {
      this.counter = 0;
      if (this.counter == 0) {
        this.counterStyle = "normal";
      }
    },
    isDivisibleBy4(number) {
      return number % 4 === 0;
    },
  },
};
</script>

<style scoped>
h1 {
  text-align: center;
  margin: 10px;
}
.counter-wrapper {
  display: flex;
  justify-content: space-around;
  align-items: center;
  flex-direction: column;
  margin: 0 auto;
  /* text-align: center; */
  padding: 20px;
  font-family: Arial, sans-serif;
  background-color: #f1f1f1;
  border-radius: 5px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
  margin-top: 20px;
  max-width: 400px;
}
button {
  cursor: pointer;
  padding: 10px 20px;
  margin: 10px;
}
.success {
  color: green;
}

.danger {
  color: red;
}

.normal {
  color: black;
}
</style>
