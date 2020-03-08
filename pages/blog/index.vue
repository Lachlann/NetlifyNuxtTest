<template>
<section>
  <article v-for="blog in blogPosts" v-bind:key="blog.title" >
    <h1>
      <a :href="`/blog/${blog.slug}`">
        {{blog.title}}
      </a>
    </h1>

  </article>

</section>
</template>
<script>
export default {
  computed: {
    blogPosts() {
      return this.$store.state.blogPosts;
    },
  },
};
</script>