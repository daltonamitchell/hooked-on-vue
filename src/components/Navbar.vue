<template>
  <nav id="navbar" v-once>
    <ul>
      <li class="logo">Hacker News</li>
      <li>new |</li>
      <li>submit</li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: 'navbar'
}
</script>

<style lang="scss" scoped>
#navbar {
  background-color: #ff6600;
  padding: 2px;
  margin-bottom: 8px;
}

li {
  display: inline-block;
}

.logo {
  font-weight: bold;
}
</style>
