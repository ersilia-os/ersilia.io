<template>
  <Section dots="false" secondary="true">
    <div class="container text-center container-sm mb">
      <h2>Ersilia Blog</h2>
    </div>
    <div class="blog-posts container container-md">
      <PostCard v-for="edge in $static.posts.edges" :key="edge.node.id" :post="edge.node"/>
    </div>
    <div class="container container-md mb">
      <Newsletter />
    </div>

    <div class="container text-center">
      <g-image width="400" alt="Ersilia logo" style="width: 150px; margin:0" src="~/assets/images/ersilia-gridsome-color.svg" />
    </div>

  </Section>
</template>

<script>
import PostCard from '@/components/PostCard.vue'
import Newsletter from '~/components/Newsletter'

export default {
  components: {
    PostCard,
    Newsletter
  }
}
</script>

<static-query>
query {
  posts: allBlogPost {
    edges {
      node {
        id
        title
        path
        date (format: "D. MMMM YYYY")
        timeToRead
        content
        author {
          id
          title
          path
          avatar (width: 60)
        }
        excerpt
      }
    }
  }
}
</static-query>
