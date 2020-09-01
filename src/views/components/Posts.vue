<template>
    <div class="posts">
        <div class="post" v-for="post in posts" :key="post._id">
            <h3>{{ post.title }}</h3>
            <h1>Hello</h1>
        </div>
        <button class="load">See More</button>
    </div>
</template>

<script>
export default {
  name: 'posts',
  props: ['posts', 'count']
}
</script>