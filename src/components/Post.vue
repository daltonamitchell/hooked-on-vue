<template>
  <li id="post">
    <span class="text-gray">{{ order }}.</span>
    <span class="upvote text-gray" @click="upvote(post.id)">▲</span>
    {{ post.description }}
    <span class="text-small text-gray">({{ post.url }})</span>
    <div class="text-small text-gray">{{ post.votes }} votes</div>
  </li>
</template>

<script>
export default {
  name: 'post',
  props: {
    post: Object,
    order: Number
  },
  methods: {
    upvote(id) {
      // let post = this.posts.find((p) => p.id === id)
      // post.votes++
      this.$emit('upvote', id)
    }
  }
}
</script>

<style lang="scss" scoped>
#post {
  padding: 2px;
}

.upvote {
  cursor: pointer;
}
</style>
