<template>
  <div class="accordion">
    <header>
      <h2>Title</h2>
      <button @click="toggle">{{ isExpanded ? "+" : "-" }}</button>
    </header>
    <p :class="{ 'show-content': isExpanded }">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Officiis, placeat
      alias? Veniam debitis, ipsum quis ex facilis sunt repudiandae ratione.
    </p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isExpanded: false,
    };
  },
  methods: {
    toggle() {
      this.isExpanded = !this.isExpanded;
    },
  },
};
</script>

<style scoped>
.accordion {
  margin-bottom: 20px;
  border: 2px solid #000;
  border-radius: 4px;
  background-color: blue;
}

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px;
}

h2 {
  font-weight: bold;
}

button {
  font-size: 18px;
  padding: 5px 10px;
  background-color: #ccc;
  border: none;
  cursor: pointer;
}

p {
  display: none;
}

.accordion .show-content {
  display: block;
}
</style>
