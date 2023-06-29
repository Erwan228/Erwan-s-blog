<template>
    <div class="blogList">
        <div v-for="blog in blogs" :key="blog.id">
            <SingleBlog :blog="blog"/>
        </div>
    </div>
</template>

<script>
import SingleBlog from './SingleBlog.vue';
export default{
    props: ['blogs'],
    components: {
        SingleBlog
    }
}
</script>

<style>

</style>