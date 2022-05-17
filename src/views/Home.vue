<template>
  <div class="home">
    <BlogPostComp :post="welcomeScreen" />
    <BlogPostComp
      :post="post"
      v-for="(post, index) in sampleBlogPost"
      :key="index"
    />
  </div>
</template>

<script>
import BlogPostComp from "../components/BlogPostComp.vue";
export default {
  name: "Home",
  components: { BlogPostComp },
  data() {
    return {
      welcomeScreen: {
        title: "WELCOME!",
        blogPost:
          "Weekly blog articles with all things programming including HTML, CSS, JavaScript and more. Register today to never miss a post!",
        welcomeScreen: true,
        photo: "coding",
      },
      sampleBlogPost: [
        {
          title: "This is a Filter Title!",
          blogHTML: "This is a filter blog post title!",
          blogCoverPhoto: "beautiful-stories",
        },
        {
          title: "This is a Filter Title!",
          blogHTML: "This is a filter blog post title!",
          blogCoverPhoto: "designed-for-everyone",
        },
      ],
    };
  },
};
</script>
