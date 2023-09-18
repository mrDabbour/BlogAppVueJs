<template>
  <div class="card" :style="{ background: background }">
    <div v-show="showMedia" class="card-media">
     <slot name="media"></slot> هنا نضيف الفتحة لعرض المحتوى المخصص
    </div>

    <div class="card-details">
      <div v-show="showHeader" class="card-header">this is title</div>
      <div v-show="showContent" class="card-content">this is content</div>
      <div v-show="showActions" class="card-actions">Actions</div>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    background: {
      type: String,
      default() {
        return "#fff";
      },
    },
    showMedia: Boolean,
    showHeader: Boolean,
    showActions: Boolean,
    showContent: {
      type: Boolean,
      default() {
        return true;
      },
    },
  },
};
</script>
<style scoped>
.card {
  background: lightblue;
  border: 2px solid #eee;
  padding: 1rem;
  border-radius: 10px;
  display: flex;
  justify-content: space-around;
  margin: 1rem auto;
}

.card:hover {
  cursor: crosshair;
  box-shadow: 1px 1px 1px 1px #eee;
}
.card-details {
  margin: 0 1rem;
}
.card-header {
  font-size: 2rem;
  margin-bottom: 1.3rem;
}

.card-content {
  font-size: 1.3rem;
  margin: 1rem auto;
}
</style>
