<template>
  <div>
    <form>
      <input type="text" placeholder="Название">
      <input type="text" placeholder="Описание">
    </form>
    <div class="post" v-for="post in posts" :key="post.id">
      <div><strong>Название:</strong> {{post.title}}</div>
      <div><strong>Описание:</strong>{{post.body}}</div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      posts: [
        {id: 0, title: 'JavaScript', body: 'Описание поста'},
        {id: 1, title: 'JavaScript1', body: 'Описание поста1'},
        {id: 2, title: 'JavaScript2', body: 'Описание поста2'},
      ]
    }
  },
  methods: {
  }
}
</script>

<style scoped>
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  .post {
    padding: 15px;
    border: 1px solid teal;
    margin-top: 15px;
  }
</style>
