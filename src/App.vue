<template>
  <div class="app">
    <post-form @create="createPost" />
    <post-list :posts="posts" @remove="removePost" />
  </div>
</template>

<script>
import PostForm from "./components/PostForm.vue";
import PostList from "@/components/PostList.vue";
export default {
  components: {
    PostForm, PostList
  },

  data() {
    return {
      posts: [
        { id: 0, title: 'JavaScript', body: 'Описание поста 1' },
        { id: 1, title: 'JavaScript1', body: 'Описание поста 2' },
        { id: 2, title: 'JavaScript2', body: 'Описание поста 3' },
      ],
    }
  },
  methods: {
    createPost(post) {
      this.posts.push(post);
    },
    removePost(post) {
      console.log('here')
      this.posts = this.posts.filter(p => p.id !== post.id)
    },
  }
}
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.app {
  padding: 20px;
}
</style>
