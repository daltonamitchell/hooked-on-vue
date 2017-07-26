<template>
  <div id="app">
    <Navbar></Navbar>
    <main>
      <PostList :posts="posts"></PostList>
    </main>
  </div>
</template>

<script>
import Navbar from './Navbar.vue'
import PostList from './PostList.vue'
import posts from '../assets/posts.json'

export default {
  name: 'app',
  components: {
    Navbar,
    PostList
  },
  data() {
    return {
      posts: posts
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  font-size: 14px;
  max-width: 85%;
  margin: 0 auto;
  background-color: #f6f6ef;
}

ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}

.text-gray {
  color: #828282;
}

.text-small {
  font-size: 11px;
}
</style>
