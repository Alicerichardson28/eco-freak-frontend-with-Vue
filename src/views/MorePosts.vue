<template>
    <div class="posts">
        <div class="post" v-for="post in post" :key="post._id">
            <h3>{{post.title}}</h3>
        </div>
    </div>
    
</template>

<script>
export default {
  data () {
    return {
      API_URL:"http://localhost:3000/api/",
      posts: [],
      postCount: 6
    }
  },
  methods: {
    getPosts () {
      fetch(this.API_URL + "posts/all")
      .then(data => {
        return data.json();
      })
      .then(json => {
          console.log(json)
        this.posts = json.result;
      })
    }
  },
  beforeMount() {
    this.getPosts();
  },
}
</script>