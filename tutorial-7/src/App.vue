<template>
  <!-- <form>
    <button @click.prevent="popUp('hi')">Click</button>
  </form> -->

  <!-- only call `submit` when the `key` is `Enter` -->
  <!-- <input @keyup.enter="submit" /> -->

  <!-- <input @input="handleInput($event)" /> -->

  <!-- <input
    @input="(e) => handleInput(e.target.value)"
    @keyup.alt.enter="clear"
    :value="name"
  /> -->

  <input
    @input="(e) => (name = e.target.value)"
    @keyup.alt.enter="clear"
    :value="name"
  />

  {{ name }}
</template>

<script>
export default {
  data() {
    return {
      name: "",
    };
  },
  methods: {
    popUp(message) {
      console.log(message);
    },
    submit() {
      console.log("Form submitted");
    },
    // handleInput(value) {
    //   this.name = value;
    //   console.log("Input:", value);
    // },
    clear() {
      console.log("Clearing input");
      this.name = "";
    },
  },
};
</script>
