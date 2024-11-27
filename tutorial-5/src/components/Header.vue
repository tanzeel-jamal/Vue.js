<template>
  <header>
    <h1>Tanzeel</h1>
    <div v-if="showContent">
      <button>Profile</button>
      <button @click="logIn()">Log in</button>
    </div>
    <div v-else>
      <button>Profile</button>
      <button @click="logOut()">Log out</button>
    </div>
  </header>
</template>

<script>
export default {
  data() {
    return {
      showContent: true,
    };
  },
  methods: {
    logOut() {
      this.showContent = true;
    },
    logIn() {
      this.showContent = false;
    },
  },
};
</script>
