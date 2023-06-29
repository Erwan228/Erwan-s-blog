<template>
    <div class="blogList">
        <div v-for="blog in blogs" :key="blog.id">
            <SingleBlog :blog="blog"/>
        </div>
    </div>
</template>

<script>
export default{
    props: ['blogs']
}
</script>

<style>

</style>