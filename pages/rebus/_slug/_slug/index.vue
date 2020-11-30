<template>
    <h1>{{ article.title }}</h1>
</template>

<script>
export default {
  async asyncData ({ $content, app, params, error }) {
    console.log(params.pathMatch)
    const path = `/${params.pathMatch || 'index'}`
    const article = await $content({ deep: true }).where({ path }).fetch()
    console.log(params.pathMatch)
    if (!article) {
      return error({ statusCode: 404, message: 'Article not found' })
    }
  
    return {
      article
    }   
  },
  mounted() {
    console.log(this.path)
  }
}
</script>