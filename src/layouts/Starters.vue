<template>
  <Layout class="has-sidebar starter-page" :footer="false">
    <div class="container flex flex-align-top">

      <div class="sidebar">

          <h3 class="menu-item" >Browse</h3>

          <g-link class="menu-item menu-link" to="/starters/">
            All Models
          </g-link>

          <h3 class="menu-item" >Inputs</h3>

          <g-link class="menu-item platform-link" v-for="item in platforms"  :key="item.node.id" :to="item.node.path" >

            {{ item.node.title }}
            <span class="platform-count" :class="{'platform-count--fade-out': item.node.belongsTo.totalCount == 0}">
              {{ item.node.belongsTo.totalCount }}
            </span>
          </g-link>

          <h3 class="menu-item" >Endpoints</h3>

          <g-link class="menu-item platform-link" v-for="item in platforms"  :key="item.node.id" :to="item.node.path" >

            {{ item.node.title }}
            <span class="platform-count" :class="{'platform-count--fade-out': item.node.belongsTo.totalCount == 0}">
              {{ item.node.belongsTo.totalCount }}
            </span>
          </g-link>

          <h3 class="menu-item" >Applications</h3>

          <g-link class="menu-item platform-link" v-for="item in platforms"  :key="item.node.id" :to="item.node.path" >

            {{ item.node.title }}
            <span class="platform-count" :class="{'platform-count--fade-out': item.node.belongsTo.totalCount == 0}">
              {{ item.node.belongsTo.totalCount }}
            </span>
          </g-link>


          <hr />

          <g-link to="mailto:hello@ersilia.io">Request a Model →</g-link>
      </div>

      <Section class="starters-content container flex-fit">
          <slot />
      </Section>
    </div>
  </Layout>
</template>

<static-query>
{
  platforms: allPlatform (order: ASC) {
    edges {
      node {
        id
        title
        path
        logo
        belongsTo {
          totalCount
        }
      }
    }
  }
}
</static-query>

<script>
export default {
  computed: {
    platforms () {
      return this.$static.platforms.edges.sort((a, b) => {
        return b.node.belongsTo.totalCount - a.node.belongsTo.totalCount
      })
    }
  }
}
</script>

<style lang="scss">
.starters-content {
  padding: var(--space-x2);
}
.platform-link {
  display: flex;
  align-items: center;
  padding: 7px 0;

  img {
    width: 25px;
    height: 25px;
    vertical-align: middle;
    margin: 0 10px 0 0;
  }
}
.platform-count {
  margin-left: auto;
  padding: 0.15rem 0.4rem;
  background-color: var(--bg-teritary);
  transition: background-color .3s;
  border-radius: .3em;
  font-size: 0.7em;

  &--fade-out {
    opacity: .3;
  }
}
</style>
