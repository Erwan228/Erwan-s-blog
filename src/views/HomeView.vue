<template>
  <div class="home">
    <h1>Home</h1>
    <h2>Blog posts</h2>
      <div class="blogs"></div>
  </div>
</template>

<script>
import { onMounted, ref } from 'vue';


export default {
  name: 'HomeView',
  components: {
    
  },
  setup() {
    const blogs = ref([])
    onMounted(() => {
      fetch('http://localhost:3000/blogs')
      .then(res => res.json())
      .then(data => this.blogs = data)
      .catch(err => console.log(err.message))
    })
    return {
      blogs,
    }
  }
}
</script>
