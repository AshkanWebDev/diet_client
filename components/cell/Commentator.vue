<script>
export default {
  props: {
    commentator: String,
    result: Number,
  },
};
</script>

<template>
  <div class="commentator">
    <p>{{ commentator }}</p>
    <p>{{ result.toFixed(2) }}</p>
  </div>
</template>

<style scoped>
.commentator {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 100px;
  height: 100px;
  border-radius: 9px;
  box-shadow: var(--shadow-1);
}
</style>
