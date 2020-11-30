<template>
    <div>
        <h1>This is _slug 1</h1>
        <article v-for="rebus in rebuser" :key="rebus.name">
            <nuxt-link :to="$route.fullPath + '/' + rebus.slug">{{ rebus.title }}</nuxt-link>
        </article>
    </div>
</template>

<script>
export default {
    
    async asyncData({ $content, params}) {
        const slug = params.slug
        const rebuser = await $content('rebus/' + slug)
        .fetch()
        
        return {
            rebuser
        }
        consol.log(slug)
    }
}
</script>