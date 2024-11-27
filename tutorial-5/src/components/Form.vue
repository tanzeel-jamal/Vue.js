<template>
  <div>
    <label for="">Name</label>
    <input type="text" />
    <div v-show="errorMessages.name">{{ errorMessages.name }}</div>
  </div>
  <div>
    <label for="">Last Name</label>
    <input type="text" />
    <div v-show="errorMessages.Lastname">{{ errorMessages.Lastname }}</div>
  </div>
  <div>
    <label for="">Password</label>
    <input type="Password" />
    <div v-show="errorMessages.password">{{ errorMessages.password }}</div>
  </div>
  <!-- <div v-if="errorMessages">
    {{ errorMessages }}
  </div> -->
  <button type="button" @click="validateForm">Submit</button>
</template>

<script>
export default {
  data() {
    return {
      //   errorMessages: null,
      errorMessages: {
        name: null,
        Lastname: null,
        password: null,
      },
    };
  },
  methods: {
    validateForm() {
      //   if (!this.errorMessages) {
      //     this.errorMessages = "Failed to validate";
      //   } else {
      //     this.errorMessages = null;
      //   }
      this.errorMessages.name = "NameError";
      this.errorMessages.Lastname = "LastNameError";
      this.errorMessages.password = "PasswordError";
    },
  },
};
</script>
