<template>
  <div class="post">
    <div class="post-header">
      <img class="user-pic" src="/profile_pics/profile_pic.jpg" alt="User">
      <p v-if="post.title" class="post-title">{{ post.title }}</p>
      <p>{{ post.content }}</p>
      <span class="post-date">{{ post.create_time }}</span>
    </div>
    <div class="post-content">
      <img class="post-image" :src="post.photo_url" alt="Post" v-if="post.photo_url">
      <p>{{ post.body }}</p>
      <button @click="incrementLikes(post.id)">Like</button>
      <span>Likes: {{ post.likes }}</span>
    </div>
  </div>
</template>

<script>
import { mapMutations } from 'vuex';

export default {
  props: {
    post: Object,
  },
  methods: {
    ...mapMutations(['incrementLikes']),
  },
};
</script>

<style scoped>
.post {
  background-color: lightgray;
  border-radius: 10px;
  padding: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  margin-bottom: 20px; /* Add margin between posts */
}

.post:first-child {
  box-shadow: none;
}

.post-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.user-pic {
  border-radius: 50%;
  width: 40px;
  height: 40px;
}

.post-date {
  color: black;
}

.post-content {
  margin-top: 10px;
}

.post-image {
  width: 100%;
  max-height: 300px;
  object-fit: cover;
  border-radius: 10px;
}

/* Add styling for the border between posts */
.posts .post + .post {
  border-top: 1px solid #c5c5c5;
}
</style>
