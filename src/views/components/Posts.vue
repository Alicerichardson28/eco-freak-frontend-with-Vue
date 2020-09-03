<template>
    <div class="posts">
        <div class="post" v-for="post in posts.slice(6, count)" :key="post._id">
            <h3>{{ post.title }}</h3>
            <h1>Hello</h1>
        </div>
        <button class="load" @click="$emit('showMore')">See More</button>
    </div>
</template>

<script>
export default {
  name: 'posts',
  props: ['posts', 'count']
}
</script>

<style lang="scss" scoped>
.posts {
    width: 100%;
    max-width: 1280px;

    margin: 50px auto;
}
    .post {
        display: block;
        padding: 15px;
        background: #ffffff;
        box-shadow: 3px 3px 8px 0px rgba(0,0,0,0.2);
        margin-bottom: 15px;
    }
.load {
        display: block;
        width: 100%;
        max-width: 180px;
        height: 40px;
        margin-left: 35em;
        outline: none;
        border: none;
        border-radius: 15px;
        appearance: none;

        background-color:  #42b983;
        box-shadow: 3px 3px 8px 0px rgba(0, 0, 0, 0.2);

        color: #171717;

        padding-top: 7px;
        box-sizing: border-box;
    }

    
</style>