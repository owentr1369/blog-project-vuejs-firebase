<template>
  <div class="blog-card-wrap">
    <div class="blog-cards container">
      <div class="toggle-edit">
        <span>Toggle Editing Post</span>
        <input type="checkbox" v-model="editPost" />
      </div>
      <BlogCardComp
        :post="post"
        v-for="(post, index) in sampleBlogCards"
        :key="index"
      />
    </div>
  </div>
</template>

<script>
import BlogCardComp from "../components/BlogCardComp.vue";
export default {
  name: "blogs",
  components: { BlogCardComp },
  computed: {
    sampleBlogCards() {
      return this.$store.state.sampleBlogCards;
    },
  },
};
</script>

<style lang="scss" scoped>
</style>