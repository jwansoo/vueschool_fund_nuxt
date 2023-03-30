<script setup>
const user = useUser();
</script>
<template>
  <div>
    <nav style="display: flex; gap: 10px">
      <nuxt-link to="/">Home</nuxt-link>
      <nuxt-link to="/movies">Movies</nuxt-link>
      <nuxt-link to="https://vueschool.io">Vue School</nuxt-link>
      <nuxt-link v-if="!user.isLoggedIn" to="/login">Login</nuxt-link>
      <a href="#" v-else @click.prevent="user.isLoggedIn = false">Logout</a>
      Test
    </nav>
    <slot></slot>
  </div>
</template>
