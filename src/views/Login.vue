<template>
  <div class="form-wrap">
    <form class="login">
      <p class="login-register">
        Don't have an account?
        <router-link class="router-link" :to="{ name: 'Register' }"
          >Register</router-link
        >
      </p>
      <h2>Login to FireBlogs</h2>
      <div class="input">
        <input type="text" placeholder="Email" v-model="email" />
        <Email class="icon" />
      </div>
      <div class="input">
        <input type="password" placeholder="Password" v-model="password" />
        <Password class="icon" />
      </div>
      <router-link class="forgot-password" :to="{ name: 'ForgotPassword' }"
        >Forgot password?</router-link
      >
      <button>Sign in</button>
      <div class="angle"></div>
    </form>
    <div class="background"></div>
  </div>
</template>

<script>
import Email from "../assets/Icons/envelope-regular.svg";
import Password from "../assets/Icons/lock-alt-solid.svg";
export default {
  components: { Email, Password },
  data() {
    return {
      email: null,
      password: null,
    };
  },
};
</script>

<style lang="scss">
</style>