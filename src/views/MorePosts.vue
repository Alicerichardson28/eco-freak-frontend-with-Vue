<template>
    <div class="posts">
        <div class="post" v-for="post in post.slice(6, count)" :key="post._id">
            <h3>{{ post.title }}</h3>
        </div>
        <button class="load">See More</button>
    </div>
    
</template>

<script>
export default {
  name: 'moreposts',
  props: ['posts', 'count']
}
</script>