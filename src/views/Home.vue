<template>
  <div class="home">
    <h2>Home</h2>
    <PostList v-if="showPosts" :posts="posts"/>
    <button @click="showPosts = !showPosts">toggle posts</button>
    <button @click="posts.pop()">remove a post</button>
  </div>
</template>

<script>
import { ref } from 'vue'
import PostList from '../components/PostList.vue'

export default {
  components: { PostList },
  name: 'Home',
  setup() {
    const posts = ref([
      { title: 'Welcome to the blog', body: 'Im baby raw denim trust fund intelligentsia keffiyeh shabby chic everyday carry blue bottle pour-over lo-fi succulents. Pabst occupy yr 8-bit selvage meditation XOXO lomo quinoa fashion axe readymade asymmetrical blog farm-to-table. Seitan heirloom live-edge, you probably havent heard of them affogato 90s flannel lumbersexual bicycle rights raw denim scenester tote bag pork belly thundercats salvia. Williamsburg crucifix iPhone, raw denim marfa helvetica truffaut man braid try-hard keytar tattooed. Shoreditch raclette post-ironic, banjo brunch intelligentsia locavore venmo prism cloud bread bitters microdosing disrupt 90s kale chips. Truffaut poke squid vaporware, vexillologist chillwave green juice mumblecore pug franzen flexitarian. Typewriter vexillologist celiac, tousled pour-over chambray activated charcoal 90s la croix swag mlkshk freegan migas trust fund +1.', id: 1 },

      { title: 'Top 5 CSS Tips', body: 'Im baby raw denim trust fund intelligentsia keffiyeh shabby chic everyday carry blue bottle pour-over lo-fi succulents. Pabst occupy yr 8-bit selvage meditation XOXO lomo quinoa fashion axe readymade asymmetrical blog farm-to-table. Seitan heirloom live-edge, you probably havent heard of them affogato 90s flannel lumbersexual bicycle rights raw denim scenester tote bag pork belly thundercats salvia. Williamsburg crucifix iPhone, raw denim marfa helvetica truffaut man braid try-hard keytar tattooed. Shoreditch raclette post-ironic, banjo brunch intelligentsia locavore venmo prism cloud bread bitters microdosing disrupt 90s kale chips. Truffaut poke squid vaporware, vexillologist chillwave green juice mumblecore pug franzen flexitarian. Typewriter vexillologist celiac, tousled pour-over chambray activated charcoal 90s la croix swag mlkshk freegan migas trust fund +1.', id: 2 }
    ])
    const showPosts = ref(true)
    
    return{ posts, showPosts }
  }
  
}
</script>
