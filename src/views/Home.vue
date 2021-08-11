<template>
  <div class="home">
    <h2>Home</h2>
    <div v-if="error">{{ error }}</div>
    <div v-if="posts.length">
      <PostList :posts="posts"/>
    </div>
    <div v-else>Loading...</div>
  </div>
</template>

<script>
import PostList from '../components/PostList.vue'
import getPosts from '../composables/getPosts'

export default {
  components: { PostList },
  name: 'Home',
  setup() {
    const { posts, error, load } = getPosts()

    load()

    return{ posts, error }
  }
  
}
</script>
