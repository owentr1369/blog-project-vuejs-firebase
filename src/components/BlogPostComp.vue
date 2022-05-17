<template>
  <div class="blog-wrapper">
    <div class="blog-content">
      <div>
        <h2 v-if="post.welcomeScreen">{{ post.title }}</h2>
        <h2 v-else>{{ post.title }}</h2>
        <p v-if="post.welcomeScreen">{{ post.blogPost }}</p>
        <p class="content-preview" v-else>{{ post.blogHTML }}</p>
        <!-- Oke -->
        <router-link class="link link-light" v-if="post.welcomeScreen" to="#">
          Login/Register
          <!-- <ArrowIcon class="arrow arrow-light" /> -->
        </router-link>
        <router-link class="link link-light" v-else to="#">
          View The Post
          <!-- <ArrowIcon class="arrow arrow-light" /> -->
        </router-link>
      </div>
      <div class="blog-photo">
        <img
          :src="require(`../assets/blogPhotos/${post.photo}.jpg`)"
          v-if="post.welcomeScreen"
          alt=""
        />
        <img
          :src="require(`../assets/blogPhotos/${post.blogCoverPhoto}.jpg`)"
          v-else
          alt=""
        />
      </div>
    </div>
  </div>
</template>

<script>
// import ArrowIcon from "../assets/Icons/arrow-right-light.svg";
export default {
  name: "blog-post",
  props: ["post"],
  // components: { ArrowIcon },
};
</script>

<style lang="scss" scoped>
</style>