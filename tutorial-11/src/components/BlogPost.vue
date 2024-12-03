<script>
export default {
  //   props: ["title", "id"],
  props: {
    title: {
      type: String,
      required: true,
    },
    id: {
      type: Number,
      required: true,
    },
    isValid: {
      type: Boolean,
    },
    tags: {
      type: Array,
      //   validator(value) {
      //     return value.every((tag) => typeof tag === "number");
      //   },
    },
    posts: {
      type: Object,
    },
  },
  computed: {
    transform() {
      return this.title.toUpperCase();
    },
    // formattedTags() {
    //   return this.tags.join(" ");
    // },
  },
};
</script>

<template>
  <h4>{{ id }} - {{ title }} - {{ isValid }} - {{ tags }}</h4>
  <span v-for="tag in tags">{{ tag }}</span>
  <!-- <h1>{{ transform }}</h1> -->
  <!-- <h1>{{ posts }}</h1> -->
</template>
