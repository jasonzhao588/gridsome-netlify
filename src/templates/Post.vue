<template>
  <BlogLayout>
    <div class="markdown-body">
      <h1>{{ $page.post.title }}</h1>
      <img :src="$page.post.thumbnail" alt="blog">
      <div v-html="$page.post.content" />
    </div>
  </BlogLayout>
</template>

<page-query>
query Post ($path: String!) {
  post: post (path: $path) {
    title
    content
    thumbnail
  }
}
</page-query>

<script>
export default {
  metaInfo() {
    return {
      title: this.$page.post.title
    }
  }
}
</script>
