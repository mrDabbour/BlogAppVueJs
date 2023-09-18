<template>
  <div>
    <h1>Hi, welcome in blog project</h1>
    <blog-button title="Go there" background="crimson" color="#fff" />
    <blog-button title="Go there" link="/blog" fullWidth />
    <card-item background="blue" :showMidea="true" :showHeader="true" :showActions="true">
      <!-- هنا نقوم باستخدام الفتحة ونضع المحتوى الذي نريد عرضه -->
         <template v-slot:media>
        <h2>This is custom media content</h2>
        <p>It can be anything you want.</p>
      </template>
    </card-item>
    <card-item background="red"> </card-item>
    <card-item></card-item>
  </div>
</template>

<script>
import BlogButton from "./components/BlogButton.vue";
import CardItem from "./components/CardItem.vue";

export default {
  name: "App",
  components: { BlogButton, CardItem },
};
</script>

<style>
#app {
}
</style>
