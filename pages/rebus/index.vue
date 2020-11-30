<template>
    <div class="container">

        <h1>Rebus typer</h1>
        <article v-for="rebus in rebuser" :key="rebus.title">
            <nuxt-link :to="$route.fullPath + '/' + rebus.slug">{{ rebus.title }}</nuxt-link>
        </article>
    </div>
</template>
<script>
export default {
    async asyncData({ $content, params, error}) {
        const rebuser = await $content('rebus')
        .fetch()
        return {
            rebuser
        }
    }
}
</script>

<style>

</style>