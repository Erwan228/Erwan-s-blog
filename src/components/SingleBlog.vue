<template>
    <div class="blog">
        <router-link :to="{ name: 'Blog', params: {id: blog.id, blog: blog}}">{{ blog.title }}</router-link>
        <p>{{ snippet }}</p>
    </div>
</template>

<script>
import { computed } from 'vue'
export default{
    props: ['blog'],
    setup(props) {
        const snippet = computed(() => {
            return props.blog.body.substring(0,100) + '....'
        })
        return {
            snippet
        }
    }
}
</script>

<style>
h3 {
    color: orange
}
</style>