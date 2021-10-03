<template>
  <div class="home">
    <BlogPost :post="welcomeScreen" />
    <BlogPost :post="post" v-for="(post,index) in sampleBlogPost" :key="index"/>
  </div>
</template>

<script>
import BlogPost from "../components/BlogPost.vue";
export default {
  name: "Home",
  components: {BlogPost},
  data() {
    return {
      welcomeScreen:{
        title:'Hoşgeldiniz',
        blogPost:
        'Haftalık blog yazıları programcılıkla ilgili herşey HTML,CSS,JavaScript ve çok daha fazlası. Bugün kayıt ve hiç bir gönderiyi kaçırma.',
        welcomeScreen:true,
        photo:'coding'
      },
      sampleBlogPost:[
        {
          title:"This is a Filler Title!",
          blogHTML:"This is a filler blog post title!",
          blogCoverPhoto:"beautiful-stories",
        },
        {
          title:"This is a Filler Title!",
          blogHTML:"This is a filler blog post title!",
          blogCoverPhoto:"designed-for-everyone",
        }
      ]
    }
  },
};
</script>

