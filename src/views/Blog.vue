<template>
    <div v-if="blog">
<h1>{{ Blog.title }}</h1>
<p>{{ Blog.body }}</p>
    </div>
    <div v-else>
        <p>Loading...</p>
    </div>
</template>

<script>
import { ref } from 'vue';
export default{
    data() {
        return{
            Blog: blog
        }
    }
}
</script>

<style>

</style>