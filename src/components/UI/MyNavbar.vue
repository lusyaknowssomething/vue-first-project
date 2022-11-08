<template>
  <div class="navbar">
    <div class="cursor" @click="$router.push('/')">Vue - учебный проект</div>
    <div class="navber__btns">
      <my-button class="cursor" @click="$router.push('/posts')">Посты</my-button>
      <my-button class="cursor" @click="$router.push('/about')">О сайте</my-button>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'my-navbar',
  }
</script>

<style scoped>
.navbar {
  height: 50px;
  background-color: lightgrey;
  box-shadow: 2px 2px 4px gray;
  display: flex;
  align-items: center;
  padding: 0 15px;
}

.navber__btns {
  margin-left: auto;
  display: flex;
  gap: 20px;
}

.cursor {
  cursor: pointer;
}
</style>
