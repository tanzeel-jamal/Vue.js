<template>
  <h1>Counter</h1>
  <div class="counter-wrapper">
    <!-- <h2 v-bind:class="{ 'default-heading': isActive, 'bg-danger': hasError }">
      Count: {{ counter }}
    </h2> -->

    <h2 v-bind:class="[isActive ? activeClass : errorClass]">
      Count: {{ counter }}
    </h2>

    <!-- @click is a event which will run on click  -->
    <button @click="incrementCounter">Increment</button>
    <button @click="decrementCounter">Decrement</button>
  </div>
</template>
<script>
export default {
  data() {
    // data always returns a object
    return {
      counter: 0, // also know as state  which contains some information
      isActive: true,
      //   hasError: true, // also know as state  which contains some information
      //   classObject: {
      //     "default-heading": false,
      //     "bg-danger": false,
      //   },
      activeClass: "default-heading",
      errorClass: "bg-danger",
    };
  },
  methods: {
    incrementCounter() {
      this.counter++;
      if (this.counter > 0) {
        // this.classObject["default-heading"] = true;
        // this.classObject["bg-danger"] = false;
        this.isActive = true;
        // this.hasError = false;
      }
    },
    decrementCounter() {
      this.counter--;
      if (this.counter <= 0) {
        // this.classObject["default-heading"] = false;
        // this.classObject["bg-danger"] = true;
        this.isActive = false;
        // this.hasError = true;
      }
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
.bg-danger {
  background-color: green;
}

.default-heading {
  color: red;
}
</style>
