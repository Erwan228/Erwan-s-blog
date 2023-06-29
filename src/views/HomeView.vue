<template>
  <div class="home">
    <h1>Home</h1>
    <h2>Blog posts</h2>
      <BlogList :blogs="blogs"/>
  </div>
</template>

<script>
import BlogList from '@/components/BlogList.vue';
import { ref } from 'vue';


export default {
  name: 'HomeView',
  components: {
    BlogList
},
  setup() {
    const blogs = ref([
      {title: "A good run", id: 1, body: "As a warrior, I tanked in the amdapor keep. As per usual I'm quite nervous about tanking since people don't seem to respect tanks, but this time it was quite enjoyable since they respected me. I got a com. A good run", tags: []}
    ])
    return {
      blogs,
    }
  }
}
</script>
