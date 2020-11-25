<template>
  <Starters>
    <h1>Ersilia A.I. Models for Global Health</h1>
    <p class="mb-x2">
      Browse, try and download our pre-trained models.
      We did our best to give credit to everyone involved in building these models.
      Please do not hesitate to <g-link to="mailto:hello@ersilia.io">contact us</g-link> should you have any claims.
      And feel free to <g-link to="mailto:hello@ersilia.io">suggest models</g-link> to us!
    </p>

    <div class="grid-cols grid-cols--3 mb">
      <StarterCard v-for="starter in $page.defaultStarters.edges" :key="starter.node.id" :node="starter.node"  />
    </div>

    <hr />

    <h3>Recent</h3>
    <div class="grid-cols grid-cols--3">
      <StarterCard v-for="starter in $page.starters.edges" :key="starter.node.id" :node="starter.node"  />
    </div>
  </Starters>
</template>

<script>
import Starters from '~/layouts/Starters.vue'
import StarterCard from '~/components/StarterCard.vue'

export default {
  components: {
    Starters,
    StarterCard
  },
  metaInfo: {
    title: 'Starters'
  }
}
</script>

<page-query>
query {
  defaultStarters: allStarter (
    sort: [{ by: "index", order: ASC }]
    filter: {
      featured: {
        eq: true
      }
    }
  ) {
    edges {
      node {
        id
        title
        path
        description
        preview
        repo
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
  },
  starters: allStarter (
    sortBy: "index"
    order: DESC
    filter: {
      featured: {
        ne: true
      }
    }
  ) {
    edges {
      node {
        id
        title
        description
        preview
        repo
        path
        screenshot  (width: 840, height:840)
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
</page-query>
