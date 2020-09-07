<template>
    <div class="blog-form">
        <h2 class="topic-form">Write your own blog</h2>
        <label class="lable-form">Title</label>
        <input type="text" placeholder="title" v-model="Blog.title">
        <label class="lable-form">Author</label>
        <input type="text" placeholder="author" v-model="Blog.author">
        <label class="lable-form">Content</label>
        <textarea placeholder="content" v-model="Blog.content"></textarea>
        <br>
        <button type="submit" @click="post">Submit</button>
    </div>
</template>

<script>
// import axios from 'axios';

export default {
  name: 'newblog',
  data() {
      return {
          Blog: { title:'', author:'',content:'' },
      }
  }, methods: {
      post:function() {
          this.$http.post('http://localhost:3000/api/post/new',{
              title: this.Blog.title,
              author: this.Blog.author,
              content: this.Blog.content
          }).then(function(data) {
          console.log(data)
      })
      }
  }
}
</script>



<style lang="scss" scoped>
    .blog-form {
            width: 600px;
            display: flex;
            flex-direction: column;
            margin: 0 auto;
            margin-bottom: 5em;
        }

        .topic-form {
            text-align: left;
        }
        .lable-form {
            text-align: left;
        }
        textarea {
            height: 200px;
        }

</style>