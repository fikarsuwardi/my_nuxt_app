<template>
  <div class="container">
    <h1>Beranda</h1>
    <ul>
      <li v-for="article in articles" :key="article.id">
        <h2>{{ article.title }}</h2>
        <p>{{ article.body }}</p>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      articles: []
    }
  },
  async fetch() {
    try {
      const response = await this.$axios.$get('/posts')
      this.articles = response
    } catch (error) {
      console.error('Error fetching articles:', error)
    }
  }
}
</script>

<style scoped>
.container {
  padding: 20px;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  margin-bottom: 20px;
}
h2 {
  margin: 0 0 10px;
}
p {
  margin: 0;
}
</style>
