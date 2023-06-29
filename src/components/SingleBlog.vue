<template>
    <div class="blog">
        <h3>{{ blog.title }}</h3>
        <p>{{ snippet }}</p>
    </div>
</template>

<script>
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