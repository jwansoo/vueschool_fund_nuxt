<template lang="">
  <form @submit.prevent="user.login">
    <h1>Login</h1>
    <label for="">
      Username
      <input type="text" />
    </label>
    <label for="">
      Password
      <input type="password" />
    </label>
    <button>Login</button>
  </form>
</template>
<script setup>
const user = useUser();
definePageMeta({
  layout: "plain",
});
</script>
<style lang=""></style>
