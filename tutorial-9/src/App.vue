<template>
  <h1>{{ count }}</h1>
  <button @click="increment">increment</button>
  <button @click="decreament">decreament</button>
  <br />
  <h3>{{ message }}</h3>
  <input v-model="form.email" type="email" placeholder="Enter email" />
  <br />
  <br />
  <input type="text" v-model="form.name" />
  <h1>{{ form.name }}</h1>
</template>
<script>
export default {
  data() {
    return {
      count: 0,
      form: {
        email: "",
        name: "",
      },
      message: "",
    };
  },
  methods: {
    increment() {
      this.count++;
    },
    decreament() {
      this.count--;
    },
  },
  watch: {
    count(newValue, oldValue) {
      if (newValue % 2 == 0) {
        console.log("number is divisible by 2");
      }
    },
    // watcher

    // "form.email"(newValue) {
    //   const regex = /[a-z0-9]+@[a-z]+\.[a-z]{2,3}/;
    //   if (regex.test(newValue)) {
    //     this.message = "Valid email address";
    //   } else {
    //     this.message = "InValid email address";
    //   }
    // },

    //deep watcher
    form: {
      handler(newValue) {
        const regex = /[a-z0-9]+@[a-z]+\.[a-z]{2,3}/;
        if (regex.test(newValue.email)) {
          this.message = "Valid email address";
        } else {
          this.message = "InValid email address";
        }
      },
      deep: true,
    },
    "form.name": {
      handler(newValue) {
        console.log(newValue);
        this.form.name = newValue.toLowerCase().replaceAll(" ", "-");
      },
    },
  },
};
</script>
