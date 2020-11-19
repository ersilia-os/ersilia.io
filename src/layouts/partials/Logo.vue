<template>
  <div class="logo">
    <g-link class="logo__link" to="/" title="Back to home">
        Ersilia Open Source Initiative
    </g-link>
  </div>
</template>

<script>
import Logo from '~/assets/images/gridsome-logo.svg'
import LogoSmall from '~/assets/images/gridsome-logo-small.svg'
export default {
  components: {
    Logo,
    LogoSmall
  },
  methods: {
    rightClick() {
      this.$router.push({ path: '/logo' })
      return false
    }
  }
}
</script>

<style lang="scss">
 .logo {
  &__svg{
  	max-width: 130px;
  	height: auto;
    margin-top: -3px;
    &--small {
      max-width: 25px;
    }
  }
 }
</style>
