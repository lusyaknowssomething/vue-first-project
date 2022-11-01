<template>
  <div>
    <h3>Список постов</h3>
    <div v-if="posts.length > 0">
      <post-item
      v-for="post in posts"
      :key="post.id"
      :post="post"
      @remove="$emit('remove', post)"
    />
    </div>
    <p v-else>Список пуст. Добавьте пост :)</p>
  </div>
</template>

<script>
import PostItem from "@/components/PostItem";
export default {
  components: {PostItem},
  props: {
    posts: {
      type: Array,
      required: true,
    }
  }
}
</script>

<style scoped>

</style>
