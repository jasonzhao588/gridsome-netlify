<template lang="html">
<div class="post">
  <h2 v-html="post.title" />
  <div v-html="post.excerpt" />
  <g-link :to="post.path" class="link">
    文章 <i class="icon icon-menu-right"></i>
  </g-link>
</div>
</template>

<script>
export default {
  props:{
    post:{
      type: Object,
      required: true
    }
  }
}
</script>

<style lang="css" scoped>
</style>
