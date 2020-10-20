<template>
    <div class="blog-form">
        <h2 class="topic-form">Write your own blog</h2>
        <label class="lable-form">Title</label>
        <input type="text"  v-model="Blog.title">
        <br>
        <label class="lable-form">Author</label>
        <input type="text"  v-model="Blog.author">
        <br>
        <label class="lable-form">Content</label>
        <textarea  v-model="Blog.content"></textarea>
        <br>
        <button type="submit" @click="post" class='submit'>Submit</button>
    </div>
</template>

<script>

export default {
  name: 'newblog',
  data() {
      return {
          Blog: { title:'', author:'',content:'' },
      }
  }, methods: {
      post:function() {
          this.$http.post('http://localhost:4000/api/post/new',{
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
            margin-left: 40em;
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
        .submit {
            margin: 0 auto;
            width: 30%;
            height: 40px;
            border-radius: 5px;
            color: white;
            background-color:  #42b956;
            border: none;
        }
</style>