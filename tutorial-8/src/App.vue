<template>
  <!-- <input :value="text" @input="(e) => (text = e.target.value)" /> -->

  <!-- <input v-model="text" /> -->
  <!-- {{ text }} -->

  <!-- {{ form }} -->
  <!-- <br /> -->
  <form>
    <!-- <label>Name</label>
    <input v-model="form.name" />
    <br />
    <label>email</label>
    <input type="email " v-model="form.email" />
    <br />

    <label>password</label>
    <input type="password" v-model="form.password" />
    <br />

    <label>confirmPassword</label>
    <input type="password" v-model="form.confirmPassword" />
    <br />

    <label>Number</label>
    <input v-model="form.number" />
    <br />

    <span>Multiline message is:</span>
    <p style="white-space: pre-line">{{ text }}</p>
    <textarea v-model="text" placeholder="add multiple lines"></textarea>
    <button type="button">submit</button> -->

    <div>Checked names: {{ checkedNames }}</div>

    <input type="checkbox" id="jack" value="Jack" v-model="checkedNames" />
    <label for="jack">Jack</label>

    <input type="checkbox" id="john" value="John" v-model="checkedNames" />
    <label for="john">John</label>

    <input type="checkbox" id="mike" value="Mike" v-model="checkedNames" />
    <label for="mike">Mike</label>
  </form>
</template>

<script>
export default {
  data() {
    return {
      text: "",
      form: {
        name: "",
        email: "",
        password: "",
        confirmPassword: "",
        number: "",
      },
      checkedNames: [],
    };
  },
};
</script>
