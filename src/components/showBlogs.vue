<template>
<div id="show-blog">
  <h2>All Blogs Post</h2>
  <div v-for="item in blogPost" class="single-blog">
      <h2>{{item.title}}</h2>
      <article>{{item.body}}</article>
  </div>
</div>
</template>

<style scoped>
#show-blog{
    max-width: 800px;
    margin:0px auto;
}
.single-blog{
    padding: 20px;
    margin:20px 0;
    box-sizing: border-box;
    background: #eee;
}
</style>

<script>

export default {
  
  data () {
    return {
        blogPost:[]
    }  
  },
  methods:{
    
  },
  created(){
      this.$http.
      get('https://jsonplaceholder.typicode.com/posts')
      .then(function(data){
          this.blogPost = data.body.slice(0,10);
      })
  }

}
</script>
