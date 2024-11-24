// CommentList.vue
<template>
  <div class="comment-list">
    <h3>Kometar</h3>
    <CommentItem
      v-for="(comment, index) in comments"
      :key="index"
      :username="comment.username"
      :comment="comment.text"
      :date="comment.date"
    />
  </div>
</template>

<script>
import CommentItem from './CommentItem.vue';

export default {
  name: 'CommentList',
  components: {
    CommentItem,
  },
  data() {
    return {
      comments: [
        {
          username: 'Rizky',
          text: 'Komensasai',
          date: '2024-11-23',
        },
        {
          username: 'Fauzi',
          text: 'Komen Ngasal',
          date: '2024-11-24',
        },
        {
          username: 'Rizky Fauzi',
          text: 'Sungguh Komen Ngasal',
          date: '2024-11-24',
        },
      ],
    };
  },
};
</script>

<style scoped>
.comment-list {
  margin: 20px 0;
}
.comment-list h3 {
  margin-bottom: 10px;
}
</style>
