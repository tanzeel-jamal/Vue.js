<template>
  <div
    v-for="({ name, description, price, tags }, index) in books"
    class="container"
  >
    <h1>{{ name }} {{ index }}</h1>
    <h1>{{ description }} {{ index }}</h1>
    <h1>{{ price }} index: {{ index }}</h1>
    <div>
      <span v-for="(tag, tagIndex) in tags"
        >{{ tag }} {{ tagIndex < tags.length - 1 ? "," : "" }}
      </span>
    </div>
    <button>BUY</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      books: [
        {
          name: "Do Epic Shit",
          description: "Motivational Book",
          price: "100",
          tags: ["rafe", "razi", "farhan"],
        },
        {
          name: "Atomic Habbits",
          description: "Motivational Book",
          price: "1000",
          tags: ["razi", "farhan"],
        },
        {
          name: "Do Epic Shit",
          description: "Motivational Book",
          price: "100",
          tags: [],
        },
      ],
    };
  },
};
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin: 20px;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 5px;
  box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
  transition: box-shadow 0.3s ease;
}
button {
  background-color: #4caf50; /* Green */
  border: none;
  color: white;
  padding: 15px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  margin: 4px 2px;
  cursor: pointer;
  border-radius: 5px;
}
</style>
