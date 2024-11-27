<template>
  <div v-if="step === 1">
    <label for="">Name</label>
    <input type="text" />
  </div>
  <div v-else-if="step === 2">
    <label for="">Email</label>
    <input type="email" />
  </div>
  <div v-else>
    <label for="">Password</label>
    <input type="Password" />
  </div>

  <button type="button" @click="backButton" v-if="step > 1">Back</button>

  <button type="button" @click="nextButton">
    {{ step <= 2 ? "Next" : "Submit" }}
  </button>
</template>

<script>
export default {
  data() {
    return {
      step: 1,
    };
  },
  methods: {
    nextButton() {
      this.step++;
      if (this.step > 3) {
        this.step = 1;
      }
    },
    backButton() {
      this.step--;
    },
  },
};
</script>
