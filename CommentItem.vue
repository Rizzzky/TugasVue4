// CommentItem.vue
<template>
  <div class="comment-item">
    <p><strong>{{ username }}</strong> - <small>{{ formattedDate }}</small></p>
    <p>{{ comment }}</p>
  </div>
</template>

<script>
export default {
  name: 'CommentItem',
  props: {
    username: {
      type: String,
      required: true,
    },
    comment: {
      type: String,
      required: true,
    },
    date: {
      type: String,
      required: true,
    },
  },
  computed: {
    formattedDate() {
      const options = { year: 'numeric', month: 'short', day: 'numeric' };
      return new Date(this.date).toLocaleDateString(undefined, options);
    },
  },
};
</script>

<style scoped>
.comment-item {
  border-bottom: 1px solid #ddd;
  padding: 10px 0;
}
.comment-item p {
  margin: 5px 0;
}
</style>
