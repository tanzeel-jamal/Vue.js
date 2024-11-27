<template>
  <h1 v-if="loading">Data is Loading</h1>
  <h1>{{ userData ? userData : errorMessage }}</h1>
</template>

<script>
export default {
  data() {
    return {
      loading: true,
      userData: null,
      errorMessage: null,
    };
  },
  methods: {
    fetchUserData() {
      setTimeout(() => {
        // this.userData = ["name", "password", "email"];
        this.loading = false;
        this.errorMessage = "Failed to fetch user data.";
      }, 2000);
    },
  },
  mounted() {
    this.fetchUserData();
  },
};
</script>
