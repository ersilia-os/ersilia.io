<template>
  <Starters>
    <h1>{{ $page.platform.title }}</h1>

    <div class="grid-cols grid-cols--3 mb">
      <StarterCard v-for="starter in $page.platform.belongsTo.edges" :key="starter.node.id" :node="starter.node"  />

      <div v-if="$page.platform.belongsTo.edges.length == 0">
        <em>Nothing here yet...</em>
      </div>
    </div>

    <hr />
    <p>
      Feel free to
      <g-link to="mailto:hello@ersilia.io">
        request
      </g-link>
      models to us!
    </p>

  </Starters>
</template>

<page-query>
query ($id: ID!) {
  platform(id: $id) {
    title
    belongsTo(sortBy: "index") {
      edges {
        node {
          ... on Starter {
            id
            title
            description
            preview
            repo
            path
            screenshot (width: 840, height: 840)
            platforms {
              title
              logo
            }
            author {
              title
              path
            }
          }
        }
      }
    }
  }
}
</page-query>

<script>
import Starters from '~/layouts/Starters.vue'
import StarterCard from '~/components/StarterCard.vue'

export default {
  components: {
    Starters,
    StarterCard
  },
  metaInfo () {
    return {
      title: `${this.$page.platform.title} starters`
    }
  }
}
</script>
