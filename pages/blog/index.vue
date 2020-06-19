<template>
  <div>
    <a
      v-for="(item, key) in blogPosts"
      :key="key"
      :href="`/blog/${item.slug}`"
    >
      {{ item.title }}
    </a>
  </div>
</template>
<script>
export default {
  computed: {
    blogPosts () {
      return this.$store.state.blogPosts
    }
  },
  mounted () {
    console.log(this.blogPosts)
  }
}
</script>
