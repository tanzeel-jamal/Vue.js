<!-- <template>
  <div v-if="show">
    <h1>tanzeel</h1>
    <h1>tan</h1>
  </div>

  <button @click="toggleShow()">toggle</button>

  <h1 v-if="name === 'tanzeel'">tanzeel</h1>
  <h1 v-else-if="name === 'tj'">tj</h1>
  <h1 v-else>oh no</h1>

  <button @click="name = !name">toggle</button>

  <button @click="toggle('tanzeel')">Tanzeel</button>
  <button @click="toggle('tj')">tj</button>
  <button @click="toggle('')">oh no</button>

  <h1 v-show="showContent">rafe</h1>
  <button @click="toggleContent()">toggleContent</button>
</template> -->

<!-- <script>
export default {
  data() {
    return {
      name: "tj",
      show: true,
      showContent: true,
    };
  },
  methods: {
    toggle(value) {
      this.name = value;
    },
    toggleShow() {
      this.show = !this.show;
    },
    toggleContent() {
      this.showContent = !this.showContent;
    },
  },
};
</script> -->

<script>
import Header from "./components/Header.vue";
import Form from "./components/Form.vue";
import MultiStepForm from "./components/MultiStepForm.vue";
import ApiData from "./components/ApiData.vue";
export default {
  components: {
    // Header,
    // Form,
    // MultiStepForm,
    ApiData,
  },
  // data() {
  //   return {
  //     showHeader: true,
  //     showForm: false,
  //     showMultiForm: false,
  //   };
  // },
  // methods: {
  //   toggleHeader() {
  //     this.showHeader = !this.showHeader;
  //   },
  //   toggleForm() {
  //     this.showForm = !this.showForm;
  //   },
  //   toggleMultiForm() {
  //     this.showMultiForm = !this.showMultiForm;
  //   },
  // },
};
</script>

<!-- <template>
  <Header v-if="showHeader" />
  <button @click="toggleHeader">Toggle Header</button>
  <br />
  <br />
  <br />

  <div v-show="showForm">
    <Form />
  </div>
  <button @click="toggleForm">Toggle Form</button>

  <br />
  <br />
  <br />
  <div v-show="showMultiForm">
    <MultiStepForm />
  </div>
  <button @click="toggleMultiForm">Toggle MultiStepForm</button>
</template> -->

<template><ApiData /></template>
