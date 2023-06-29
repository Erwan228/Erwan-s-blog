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
      {title: "A wondeful run", id: 1, body: "I was tanking as gunbreaker in Amaurot. The team was incompetent, but patient. I often ended up soloing the bosses. Specifically the first and last. The last one was such an ordeal, with careful mitigations and potions. I was sweating, and running low on potions. I finished with two potions left. During the whole solo battle, which was from above 50%, the team rooted for me in the chat. That felt so wonderful", tags: ["GNB", "Tank", "Amaurot", "Dungeon", "Good"]},
      {title: "A bad run", id: 2, body: "As a warrior, I tanked in the amdapor keep. As per usual I'm quite nervous about tanking since people don't seem to respect tanks, and this time was a bad run. People kept running ahead, pulling more mobs. The healer couldn't keep up.", tags: ["WAR", "Tank", "Dungeon", "Bad", "Amdapor keep"]},
      {title: "A fun exploration", id: 3, body: "With my friends Toranin, Kuroi and Merle, we took another shot at Eureka orthos. During our expedition we encountered a unique situation, which we kinda wanted to have commisioned.", tags: ["Deep dungeon", "Friends", "Eureka orthos", "Social", "Good"]},
      {title: "A frustarting run", id: 4, body: "Another crystal tower run. Im so sick of these, and the people who appereantly want to do these ones but can't fucking do any mechanics.", tags: ["Alliance raid", "Bad", "Rant", "Strong language"]},
    ])
    return {
      blogs,
    }
  }
}
</script>
