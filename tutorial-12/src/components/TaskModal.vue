<template>
  <div class="modal">
    <div class="modal-content">
      <div class="model-heading">
        <h2>Modal Title</h2>
        <button @click="$emit('closeModel')">Close</button>
      </div>
      <div class="modal-body">
        <label>Title</label>
        <input
          type="text"
          placeholder="Enter your task title"
          v-model="newData.title"
        />
        <label>Description</label>
        <textarea
          placeholder="Enter your task description"
          v-model="newData.description"
        ></textarea>
      </div>
      <div class="modal-footer">
        <button @click="$emit('closeModel')">Cancel</button>
        <button @click="submitForm">Add</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  emits: ["closeModel", "submitForm"],
  data() {
    return {
      newData: {
        title: "",
        description: "",
      },
    };
  },
  methods: {
    submitForm() {
      this.$emit("submitForm", this.newData);
    },
  },
};
</script>

<style scoped>
.modal {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  z-index: 1000;
}
.modal-content {
  background-color: white;
  margin: 15% auto;
  padding: 20px;
  border-radius: 8px;
  width: 50%;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}

.modal .modal-content .model-heading {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.modal .modal-content .model-heading button {
  padding: 10px 20px;
  font-size: 16px;
  cursor: pointer;
}
.modal .modal-content .modal-body {
  margin-top: 20px;
}
.modal .modal-content .modal-body label,
input,
textarea {
  display: block;
  width: 100%;
  margin: 5px;
  padding: 5px;
}

.modal .modal-content .modal-footer button {
  margin-right: 10px;
  padding: 10px 20px;
  font-size: 16px;
  cursor: pointer;
}
</style>
