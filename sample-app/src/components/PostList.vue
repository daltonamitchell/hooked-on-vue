<template>
  <div id="post-list">
    <ul class="posts">
      <Post
        v-for="(post, index) in sortedPosts"
        :post="post"
        :order="index + 1"
        :key="post.id"
        @upvote="handleUpvote"
      ></Post>
    </ul>
  </div>
</template>

<script>
import Post from './Post.vue'

export default {
  name: 'post-list',
  components: {
    Post
  },
  props: {
    posts: Array
  },
  computed: {
    sortedPosts() {
      return this.posts.sort((a, b) => b.votes - a.votes)
    }
  },
  methods: {
    handleUpvote(id) {
      let post = this.posts.find(p => p.id === id)
      post.votes++
    }
  }
}
</script>

<style lang="scss" scoped>
</style>
