<template>
  <div class="card">
    <header>
      <img class="avatar" width="40" height="40" :alt="user.name" :src="user.img">
      <p class="name">fred</p>
    </header>
    <footer>
      <input class="search" type="text" placeholder="search user...">
    </footer>
  </div>
</template>

<script>
import { actions } from '@/store/index.js'
export default {
  vuex: {
    actions: actions,
    getters: {
      user: ({ user }) => user,
      filterKey: ({ filterKey }) => filterKey
    }
  },
  methods: {
    onKeyup (e) {
      this.search(e.target.value)
    }
  }
}
</script>

<style scoped>
</style>
