<template>
  <div id="app">
    <div>
      <router-link to="/">Home</router-link>
      <router-link to="/users">Users</router-link>
      <router-link to="/users/10">Users 10</router-link>
    </div>
    <hr>
    <router-view></router-view>
    <hr>
    <app-message></app-message>
  </div>
</template>

<script>
export default {
  data () {
    return {
    }
  }
}
</script>

<style lang="scss">
</style>
