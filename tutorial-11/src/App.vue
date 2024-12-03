<script>
import BlogPost from "./components/BlogPost.vue";
export default {
  components: {
    BlogPost,
  },
  data() {
    return {
      posts: [
        {
          id: 1,
          title: "My journey with Vue",
          author: "Razi",
          isValid: true,
          tags: [1, 2, 3, 4, 5],
        },
        {
          id: 2,
          title: "Blogging with Vue",
          author: "Rafe",
          isValid: false,
          tags: [1, 2, 3, 4, 5],
        },
        {
          id: 3,
          title: "Why Vue is so fun",
          author: "Farhan",
          isValid: true,
          tags: [1, 2, 3, 4, 5],
        },
      ],
    };
  },
};
</script>
<template>
  <BlogPost
    v-for="post in posts"
    :title="post.title + ' by ' + post.author"
    :id="post.id"
    :isValid="post.isValid"
    :tags="post.tags"
  />
  <!-- <BlogPost :posts="posts" /> -->
</template>
